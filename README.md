// Change date format from html input to something like '12 May 2018'
function changeFormat($date){
	$date_array = [];

	// strip '-' from date 
	$split_date = explode('-', $date);

	foreach ($split_date as $key => $value) {

		if ($key == 1) {
			// Convert months to words
			if ($value == '01') {
				$date_array[] = 'January';
	
			} elseif ($value == '02') {
				$date_array[] = 'Febuary';
				
			} elseif ($value == '03') {
				$date_array[] = 'March';
				
			} elseif ($value == '04') {
				$date_array[] = 'April';
				
			} elseif ($value == '05') {
				$date_array[] = 'May';
				
			} elseif ($value == '06') {
				$date_array[] = 'June';
				
			} elseif ($value == '07') {
				$date_array[] = 'July';
				
			} elseif ($value == '08') {
				$date_array[] = 'August';
				
			} elseif ($value == '09') {
				$date_array[] = 'September';
				
			} elseif ($value == '10') {
				$date_array[] = 'October';
				
			} elseif ($value == '11') {
				$date_array[] = 'November';
				
			} elseif ($value == '12') {
				$date_array[] = 'December';
				
			}
		} else {
			$date_array[] = $value;
		}
	}

	// $pickup_date = implode(' ', $date_array);
	$pickup_date = implode(' ', array_reverse($date_array));

	return $pickup_date;
}
