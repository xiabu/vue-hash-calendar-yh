本项目基于 vue-hash-calendar，api 文档等请参考 https://github.com/TangSY/vue-hash-calendar

isFillLastDays，渲染周数（非 6 行）
isWeekSetMonthDay，周视图时非本月不置灰

// 在日历后面填充下个月的日期，补齐 6 行 7 列
let fillDays = this.calendarDaysTotalLength - calendarOfCurrentMonth.length;
// 只补齐最后一行
if (fillDays >= 7 && this.isFillLastDays) {
fillDays = 7 - (calendarOfCurrentMonth.length % 7)
}

if (this.isShowWeek && this.isWeekSetMonthDay) {
return false
} else {
let dateOfCurrentShow = this.calendarOfMonth[index][15]; // 本月中间的日期一定为本月
return (
date.year !== dateOfCurrentShow.year ||
date.month !== dateOfCurrentShow.month
);
}
