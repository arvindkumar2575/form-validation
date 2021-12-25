> Form Input data validation library with form

# add class in input tag as follows

## for all inputs except radio buttons and checkboxs
- if input/textarea is require feild then add **fieldRequired** as className in that input and put it into div element as shown below
```html
<div>
    <label>Username</label>
    <input type="text" name="name" class="fieldRequired" data-errormessage="Please enter your username" />
</div>
```

- if input is number feild then add **numberRequired** as className in that input and put it into div element as shown below
```html
<div>
    <label>Mobile No</label>
    <input type="text" name="name" class="numberRequired" data-errormessage="Please enter your mobile no" />
</div>
```

- if input is email feild then add **emailRequired** as className in that input and put it into div element as shown below
```html
<div>
    <label>Email Id</label>
    <input type="text" name="email" class="emailRequired" />
</div>
```

- if input is select feild with options as a dropdown then add **optionRequired** as className in that select tag and put it into div element as shown below
```html
<div>
    <label>Select 1 Car</label>
    <select name="cars" class="optionRequired" data-errormessage="Please select">
        <option value="none">--select--</option>
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="mercedes">Mercedes</option>
        <option value="audi">Audi</option>
    </select>
</div>
```

## for radio buttons & checkboxs
- put all the radio buttons inside a div element & give class of **radiobuttonRequired** and put input[type="radio"] inside it
```html
<div>
    <label>Select Gender</label>
    <div class="radiobuttonRequired" data-errormessage="Please click one">
        <label><input type="radio" name="gender" value="male">
            Male</label>
        <label><input type="radio" name="gender" value="female">
            Female</label>
        <label><input type="radio" name="gender" value="other">
            Other</label>
    </div>
</div>
```

- put all the radio buttons inside a div element & give class of **checkboxRequired** and put input[type="checkbox"] inside it.
```html
<div>
    <label>Select Profession</label>
    <div class="checkboxRequired">
        <label><input type="checkbox" name="profession" value="Student">
            Student</label>
        <label><input type="checkbox" name="profession" value="Teacher">
            Teacher</label>
        <label><input type="checkbox" name="profession" value="Administrator">
            Administrator</label>
        <label><input type="checkbox" name="profession" value="Others">
            Others</label>
    </div>
</div>
```


> ***Note:*** You can add custom error values 
1. you just need to add **data-errormessage** attribute in that same element in which you add classes for data validation like above.

2. you can add second argument as **object** with object of attribute name as key in the same function in which you send the form for validation like i do in form.html file at line no 139
```javascript
    {
        username: {
            error: "Username error"
        },
        phoneno: {
            error: "phone no error"
        },
        profession: {
            error: "profession error"
        },
    }

```


Style them as per your need by selecting that element by its parent as I do in this files