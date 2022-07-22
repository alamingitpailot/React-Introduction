# React
# React install and problem solve
# Components create
# React State
# Map and Props
## React কি ?
### React হচ্ছে javascript libary, React হচ্ছে components Base
## React দিয়ে কি হয় ?
### ওয়েব সাইট user interface তৈরি করে হয় । single page Application React ব্যবহার করে হয় । 
# কিছু Command মনে রাখার দরকার --
## যদি আগে থেকে প্রোজেক্ট থাকে তাহলে 
* cd (Folder Name)
* npm start

# Visual Studio তে কোড লিখার সময় কিছু শর্টকাট ব্যবহার করবো
😍 rcc press করলে ফুল একটা Components Visual Code editor আমাদের কে দেয় ।


# -----------------------------------
# Map কি ?
## React loop হিসেবে ব্যবহার করা হয় । Map টা একধরণের লুপ ।
# Props কি ?
## Props মাধ্যমে value transfer করা যায় । value Assign করা যায়
 
# setState কি ?
## বাংলায় বলতে গেলে State value পরিবতন করা যায় । 
### নিচে ছোট একটা উদাহরণ দেওয়া হল 

```
class App extends Component {
state ডিফাইন করে দিলাম null
Input ভালুএ কে পাসস করাবো 
  state = {
    inputText:''
  }

  testHandle = (e) => {
    this.setState({ inputText: e.target.value }); Input ভালুএ কে পাসস করে দিলাম 
    প্রথমত null ছিল setState দিয়ে value change করায় দিলাম । 
    console.log(this.state.inputText); state Value কে console.log korlam
  }

  render() {
    return (
      <div> 
        <form action="" method="">
          <input type="text" placeholder='input text' onChange={this.testHandle} />
        </form>
      </div>
    )
  }
}
export default App;

```

# React styleing
### প্রথমত আমি inline css ব্যবহার করবো । 
### নিচে ছোট একটি উদাহরন দিলাম 
````
class App extends Component {
  render() {
    return (
      <div>
        <h1>Style in React</h1>
        <button style={btnStyle}>Button Style</button>

      </div>
    )
  }
}
const btnStyle = {
    color: "white",
    background: 'red',
    padding: '10px',
    borderRadius: '3px',
    border:'none'
}
export default App;

````
* আভাবে আমরা inline css ব্যবহার করি 

## React External css ব্যবহার করতে পারি 

* এই কাজ টুকু করার মাধ্যমে ExportVariable কি ভাবে কাজ করে তা জানতে পারছি । 
* Style.js ভিতরে আমি css গুলি লিখি তারপর App.js ব্যবহার করি 
* css লিখার মাধ্যমে module.exports করা হয় । 

```
const btnStyle = {
    color: "white",
    background: 'red',
    padding: '10px',
    borderRadius: '3px',
    border:'none'
}
  
module.exports = {
    btnStyle:btnStyle
}


```
* Style.js ফাইল কে import করে নিতে হবে । 
* module.exports যেই নাম তা দেওয়া হয় সেই নাম তা app.js ব্যবহার করলেই style গুলি পেয়ে যায় । 

```
var { btnStyle } = require('./Styles');
class App extends Component {
  render() {
    return (
      <div>
        <h1>Style in React</h1>
        <button style={btnStyle}>Button Style</button>
      </div>
    )
  }
}

export default App;
```


