# Laravel-Notes



    return view('profile',array('user'=>Auth::user()))->with('years',Group::all())->with('occupations',Occupation::all());



















