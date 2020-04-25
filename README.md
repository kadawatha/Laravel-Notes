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
<p>Laravel Auth in Controller </p>

``` 
public function allOrders(){

        $user = Auth::user();
        
        $id = Auth::id();
        
        $Orders=DB::select("SELECT * FROM orders WHERE users_id = '$id'");
        return view('checkout.review_order_2',compact('Orders','user'));
        
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



<hr>


<p> authentication genarate Laravel 6 </p>



```

composer require laravel/ui "^1.0" --dev

php artisan ui vue --auth


```

<h3> Laravel Active Manu  </h3>

```

     <div class="menu">
                <div id="cssmenu">
                    <ul>
                        <li class="{{(request()->segment(1) == '') ? 'active' : '' }}"><a href="{{url('/')}}"><span>Home</span></a></li>
                        <li class="{{(request()->segment(1) == 'about') ? 'active' : '' }}"><a href="{{url('about')}}"><span>About</span></a></li>
                        <li class="{{(request()->segment(1) == 'gallery') ? 'active' : '' }}"><a href="{{url('gallery')}}"><span>Gallery</span></a></li>
                        <li class="{{(request()->segment(1) == 'contact-page') ? 'active' : '' }}"><a href="{{url('contact-page')}}"><span>Contact</span></a></li>
                    </ul>
                </div>
    </div>
            

```

<p> variable inside asset </p>

```
{{ asset('img/backgrounds/' . $background . '.jpg') }}

```




