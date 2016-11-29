### This is a simple vue modal component.

* Install & Usages

> npm install vue-modalx

in your vue component:

```javascript
<template>
  <div>
    <button @click="options.show = true"></button>
    
    <Modal :options="options"></Modal>
    
    <Modal :options="options">
      <h4>Modal Body Part</h4>
      <div>
        write whatever you like :)
      </div>
      
    </Modal>
    
  </div>
</template>


<script>

  import Modal from 'vue-modalx'

  export default {
    //.... other vue options
    data: {
      options: {
        show: false,  // required, 
        showBody: false, // true  by default
        showFooter: true, // true  by default
        showHead: true, // true  by default
        backdrop: 'static',// 'static' | 'normal'(by default)
        width: '300', //width 'px'
        title: 'Test Modal',
        theme: 'danger', // 'primary'(by default) | 'success' | 'danger' | 'info' | 'warning' | 'default'
        OkText: 'OKTest', // 'OK' by default
        CancleText: 'Close', // 'Cancle' by default
        onOkHandler () {
          this.show = false
        },
        onCancleHandler () {
          this.show = false
        },
      }
    },
    components: {
      Modal
    }
  }
  
</script>
```

You can also use it in your render function :)

