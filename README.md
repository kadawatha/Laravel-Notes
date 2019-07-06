# Laravel-Notes



    return view('profile',array('user'=>Auth::user()))->with('years',Group::all())->with('occupations',Occupation::all());



laravel foreach loop in controller



```
foreach ($product as $p) {
echo $p->sku;
}
```

















