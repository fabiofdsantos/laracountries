# Laracountries
Migration and seed files with all countries for Laravel PHP Framework.

The country codes are in the format [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2).

## A Simple Example of Use
#### Controller
```php
	/**
	* Show the form for creating a new resource.
	*
	* @return View
	*/
	public function create()
	{
		$countries = Country::all();

		return View::make('myview', compact('countries'));
	}
```
#### View
```php
    <select class="form-control" name="country">
        <option value="">Select a country</option>
        @foreach($countries as $country)
            <option value="{{ $country->id }}">{{ $country->name }}</option>
        @endforeach
    </select>
```

## License
Copyright (c) 2015 [Fábio Santos](http://www.fabiosantos.me). See the LICENSE
file for license rights and limitations (MIT).
