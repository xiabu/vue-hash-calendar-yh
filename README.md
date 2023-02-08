本项目基于 vue-hash-calendar，只优化渲染周数（非 6 行），api 文档等请参考 https://github.com/TangSY/vue-hash-calendar

// 在日历后面填充下个月的日期，补齐 6 行 7 列
let fillDays = this.calendarDaysTotalLength - calendarOfCurrentMonth.length;
// 只补齐最后一行
if (fillDays >= 7 && this.isFillLastDays) {
fillDays = 7 - (calendarOfCurrentMonth.length % 7)
}
