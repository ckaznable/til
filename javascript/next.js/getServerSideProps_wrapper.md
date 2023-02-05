# getServerSideProps包裝

不要用方法同時產出`getServerSideProps`跟`page component`不然產出的邏輯會一起被打包到前端

```javascript
export function getPageWrapper() {
  return {
     getServerSideProps() {
        return {
           props: {}
        }
     },
    component() {
      return <></>
    }
  }
}
```

需要包裝`getServerSideProps`時跟`page component`包裝分開

```javascript
export function getServerSidePropsWrapper() {
  return {
    props: {}
  }
}

export function getPageComponentWrapper() {
  return <></>
}
```
