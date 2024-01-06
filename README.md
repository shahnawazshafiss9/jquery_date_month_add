# Jquery Add Month by Number of days 
```javascript
function addMonthsByDays(date, number_of_days) {
           var select_date_split = date.split('-'); 
           var select_date_split_arr = select_date_split[2] + '-'+ select_date_split[1] +'-'+ select_date_split[0];
           var currentDate = new Date(select_date_split_arr);
           var d = currentDate.getDate();
           currentDate.setDate(currentDate.getDate() + +number_of_days);
            if(type =='asc'){
               return ('0' + currentDate.getDate()).slice(-2) + '-' + ('0' + (currentDate.getMonth() + 1)).slice(-2) + '-' + currentDate.getFullYear();
            }else{
               return currentDate.getFullYear() + '-' + ('0' + (currentDate.getMonth() + 1)).slice(-2) + '-' + '0' + ('0' + currentDate.getDate()).slice(-2);
            }
        }
```

# Jquery Add Month by Number of Month

```javascript
        function addMonthsByMonth(date, months, type='asc') {
           var select_date_split = date.split('-'); 
           var select_date_split_arr = select_date_split[2] + '-'+ select_date_split[1] +'-'+ select_date_split[0];
           var currentDate = new Date(select_date_split_arr); 
           currentDate.setMonth(currentDate.getMonth() + months); 
            if(type =='asc'){
               return ('0' + currentDate.getDate()).slice(-2) + '-' + ('0' + (currentDate.getMonth() + 1)).slice(-2) + '-' + currentDate.getFullYear();
            }else{
                return currentDate.getFullYear() + '-' + ('0' + (currentDate.getMonth() + 1)).slice(-2) + '-' + '0' + ('0' + currentDate.getDate()).slice(-2);
            }
           
        }
```
# Jquery diff two number of days

```javascript

        function diffDateByDate(date1, date2){
            var date_1 = new Date(date1);
            var date_2 = new Date(date2);
            if (date_1 instanceof Date && !isNaN(date_1.valueOf()) && date_2 instanceof Date && !isNaN(date_2.valueOf())) {
                console.log('date_1' + date_1);
                console.log('date_2' + date_2);
                var timeDiff = date_1.getTime() - date_2.getTime();
                console.log('timeDiff' + timeDiff);
                var daysDiff = Math.ceil(timeDiff / (1000 * 3600 * 24));
                return daysDiff;
            }else{
                console.log('The value is a not valid date.');
                console.log('date_1' + date_1);
                console.log('date_2' + date_2);
            } 
        }
```
