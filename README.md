# Laravel-Notes

<h5> Laravel Old Version Download </h5>

# composer create-project laravel/laravel your-project-name 5.0

<hr>
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


    php artisan make:model Sample -mcr


<hr>


    php artisan make:model Category -m







