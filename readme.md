### klassjs


It's a simple way to create classes with static, public and private methods/variables with the support of annotations.

### Example

All the files are under the example folder

```javascript
require ('../klass.js');
require ('./helloworld.js');
require ('./annotations/action.js');

var hw = new HelloWorld();
    hw.sayHi('poste9')
      .sayHello();

for(var key in hw)
{
    if (hw[key].hasAnnotation(Action))
    {
        console.log(key + " is an action!")
    }
    else
    {
        console.log(key + " is not an action!")
    }
}

/**
 * Expected out:
 Hi poste9
 Hello poste9
 sayHi is an action!
 sayHello is not an action!

 Process finished with exit code 0
 */
 ```
