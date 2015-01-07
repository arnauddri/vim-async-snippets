vim-async-snippets
===================

Vim snippets for most commonly used async functions

## Install

Place ```javascript.async.snippets``` in ```~/vim/snippets``` and that's it.

## async.each

Type 'aseach' and get:
```javascript
	async.each(
		${1:array},
		function(${2:item}, callback){
			${3:callback();}
		},
		function(err){
			if(err)
				${4}
		}
	);
```

## async.eachseries

Type 'aseachseries' and get:
```javascript
	async.eachSeries(
		${1:array},
		function(${2:item}, callback){
			${3:callback();}
		},
		function(err){
		if(err)
			${4}
		}
	);
```

## async.map

Type 'asmap' and get:
```javascript
	async.map(
		${1:array},
		function(${2:item}, callback){
			${3:callback();}
		},
		function(err){
			if(err)
				${4}
		}
	);
```

## async.parallel

Type 'asparallel' and get:
```javascript
	async.parallel({
		${1:one}: function(callback){
			${2://body}
		},
		${3:two}: function(callback){
			${4://body}
		},
	},
	function(err, ${5:results}) {
		${6}
	});
```

## async.series

Type 'asseries' and get:
```javascript
	async.series({
		${1:one}: function(callback){
			${2:callback(null,{})}
		},
		${3:two}: function(callback){
			${4:callback(null,{})}
		},
	},
	function(err, ${5:results}) {
		${6}
	});
```

## async.waterfall

Type 'aswaterfall' and get:
```javascript
	async.waterfall([
		function(callback){
			callback(null, ${1:'one'}, ${2:'two'});
		 ,
		function(${3:arg1}, ${4:arg2}, callback){
			callback(null, ${5:'three'});
		},
		function(${6:arg1}, callback){
			callback(null, ${7:'done'});
		}
	], function (err, ${8:result}) {
		${9}
	});
```
