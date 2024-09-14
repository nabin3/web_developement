* Form controls live inside a <form> element. This element should always carry the action attribute and will usually have a method and id attribute too.

```bash
<form action="http://www.example.com/subscribe.php"  method="get">  
    <p>This is where the form controls will appear.</p>
</form>
```

* The <input> element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.
```bash
<form action="http://www.example.com/login.php">  
    <p>Username:
        <input type="text" name="username" maxlength="30" />  
    </p> 
</form> 
```

* The <textarea> element is used to create a mutli-line text input. Unlike other input elements this is not an empty element. It should therefore have an opening and a closing tag.

* type="radio" Radio buttons allow users to pick just one of a number of options. The checked attribute can be used to indicate which value (if any) should be selected when the page loads. The value of this attribute is checked. Only one radio button in a group should use this attribute.
```bash
<form action="http://www.example.com/profile.php">  
    <p>Please select your favorite genre:
        <br />  
        <input type="radio" name="genre" value="rock"  checked="checked" /> Rock  
        <input type="radio" name="genre" value="pop" />  Pop  
        <input type="radio" name="genre" value="jazz" />  Jazz  
    </p> 
</form> 
```

