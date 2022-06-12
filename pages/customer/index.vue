<template>
  <div>
    <h1 class="tw-text-3xl tw-mb-5">จัดการสมาชิก</h1>
    <CustomDataTable
      :table-headers="tableHeaders"
    ></CustomDataTable>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        tableHeaders: [
          {
            text: 'เบอร์ติดต่อ',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'ชื่อบัญชี', value: 'calories' },
          { text: 'เลขบัญชี', value: 'fat' },
          { text: 'ธนาคาร', value: 'carbs' },
          { text: 'สถานะบัญชี', value: 'protein', align: 'center' },
          { text: 'สถานะ', value: 'iron', align: 'center' },
          { text: '', value: 'actions', sortable: false, class: 'thin-cell', cellClass: 'thin-cell' },
        ],
      }
    },
    mounted () {
      console.log(this.tableHeaders)
    },
  }
</script>
