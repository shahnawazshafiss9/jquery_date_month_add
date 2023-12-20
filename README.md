# jquery_date_month_add

    var number_of_days = $('#number_of_days').val();
    var select_date = $('#select_date').val();
    var select_date_split = $('#select_date').val().split('-');
    var select_date_split_arr = select_date_split[2] + '-'+ select_date_split[1] +'-'+ select_date_split[0];
    
function addMonths(date, months) {
        var d = date.getDate();
        date.setMonth(date.getMonth() + +months);
        if (date.getDate() != d) {
            date.setDate(0);
        }
        return date.getFullYear() + '-' + ('0' + (date.getMonth() + 1)).slice(-2) + '-' + ('0' + date.getDate()).slice(-2);
    }
var print_date = addMonths(new Date(select_date_split_arr), number_of_days);
    console.log(print_date);
