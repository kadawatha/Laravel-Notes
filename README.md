# Laravel-Notes



    return view('profile',array('user'=>Auth::user()))->with('years',Group::all())->with('occupations',Occupation::all());



laravel foreach loop in controller



```
foreach ($product as $p) {
echo $p->sku;
}
```


How do we set a custom port for test server? (microservice)

 php artisan serve --port=8080

<hr>

php artisan serve --port=8001


<hr>








