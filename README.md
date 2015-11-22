# CodeIgniter-cURL

## !!! DEPRECATED !!!
** This package a fork of https://github.com/philsturgeon/codeigniter-curl
** with the addition for a curl_multi support, check the last function of the model
** Phil has stopped support for this library and I do not promise any support, use at your own risk

[Guzzle]: http://guzzlephp.org
[Requests]: http://requests.ryanmccue.info/

CodeIgniter-cURL is a CodeIgniter library which makes it easy to do simple cURL requests 
and makes more complicated cURL requests easier too.


## Usage of curl_multi
Simply, call $this->curl->multiRequest($requests,$options) from your controller.

## Structure of $requests
### for get requests
#### (minimal)
`$requests = array( 
	'url' => URL_OF_THE_GET_REQUEST,
);`

### for other requests (post,delete,put)
#### (minimal)
`$requests = array( 
	'url' => URL_OF_THE_REQUEST,
	'method_name_here' => array(""),  //Replace the word method_name_here with put or delete or post
);`
#### advanced with parameters
`$requests = array( 
	'url' => URL_OF_THE_REQUEST,
	'method_name_here' => array(  //Replace the word method_name_here with put or delete or post
		'param1' => value1,
		'param2' => value2,
	),  
);`

### Structure of $options
#### Example
`$options = array(
	'CURLOPT_RETURNTRANSFER' => 1,
	'CURLOPT_SSL_VERIFYPEER' => 0,
	'CURLOPT_FAILONERROR' => 0,
);
`