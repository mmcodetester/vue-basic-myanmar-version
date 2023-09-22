# VUE JS MYANMAR


### VUE JS
1. javascript framework for building user interfaces.
2. build on top standard HTML, CSS, Javascript
3. provide declarative and component based programming model to develop your UI.

### declarative rendering
1. extends with HTML standard templates
2. allows declarative describe HTML output based on javascript state

### reactive
1. automatically tracks JavaScript state changes
2. efficiently updates the DOM when the state change

### Document Object Model (DOM)
DOM (Document Object Model) ဆိုတာ Web Document အတွက် HTML,XML Document တို့လိုမျိုး tree-like structure programming interface တစ်ခုပဲဖြစ်ပါတယ်။ DOM ဟာ programs တွေ scripts တွေကို dynically access လုပ်ပေးပြီး၊ web document ရဲ့ content တွေ structure တွေ style တွေကို manipulate လုပ်ပေးနိုင်တယ်။ Vue Js ဟာ DOM ကိုသုံးထားပြီးတော့ UI ကို manipulate လုပ်နေတယ် ပြီးတော့ data state တစ်ခုခု changes ဖြစ်တိုင်းအလိုအလျှောက် Update လုပ်ပေးတဲ့  framework တစ်ခုဖြစ်တယ်။ Vue Js မှာ DOM က application's data နဲ့ UI ကို Synchronization လုပ်ပြီး changes တစ်ခုဖြစ်တာနဲ့ UI ရော data ကိုရော Update လုပ်ပေးတယ်။
### Component Structure
Vue js မှာ application တွေကို component တွေသုံးပြီး create လုပ်တယ်။ Components တွေဟာ reusable ဖြစ်တယ်၊ encapsulated units တွေဖြစ်တယ်။ Component တွေဟာ ကိုယ်ပိုင် template ၊ logic နဲ့ style တွေရှိတယ်။
### Encapsulation
Encapsulation is a way to restrict the direct access to some components of an object, so users cannot access state values for all of the variables of a particular object. Encapsulation can be used to hide both data members and data functions or methods associated with an instantiated class or object.
### Template 
vue ရဲh Component တစ်ခုချင်းစီတိုင်းမှာ HTML structure ကို define လုပ်ပေးတဲ့ template တစ်ခုရှိတယ်။ အဲ့ဒီ template ထဲမှာဆိုရင် veu ရဲ့ သက်ဆိုင်ရာ directive တွေနဲ့ expression တွေပါဝင်တယ်။ ပြောရမယ်ဆိုရင် vue မှာ component တစ်ခု create လုပ်မယ်ဆိုရင် <code>&lt;template&gt;&lt;/template&gt;</code>ကိုသုံးပြီး create လုပ်ရမယ်။ element တွေကို template အဖွင့်အပိတ်အတွင်းမှာရေးရမယ်။
<pre>
    <code>
       &lt;template&gt;
            &lt;p&gt; Hello VUE ! &lt;/p&gt;
        &lt;/template&gt;
    </code>
</pre>
### Data State
Vue JS မှာ data state ဆိုတာ UI နဲ့ data အကြား reactive ဖြစ်အောင်၊ ထိရောက်စွာ render လုပ်ပေးနိုင်အောင် ရှင်းရှင်းလင်းလင်းပိုင်းခြားပေးထားတဲ့ concept တစ်ခုပဲဖြစ်ပါတယ်။ Data ဆိုတာ component ရဲ့ initial state ဖြစ်ပြီး 'data' function ထဲမှာ return လုပ်ထားတဲ့ variables တွေ properties တွေဖြစ်ပါတယ်။ user input ကြောင့်ဖြစ်ဖြစ် api response ကြောင့်ဖြစ်ဖြစ် 'data'function ရဲ့အခြားပြင်ပ functionတွေကြောင့် data properties တွေ changes ဖြစ်သွားတာမျိုးကို state လို့ခေါ်ပါတယ်။ တစ်နည်းအားဖြင့် data state changes ဖြစ်တယ်ပေါ့။
### Data (Initial State)
<pre>
    <code>
        export default{
            data(){
                return{
                    //initial data state
                    message:'Hello Vue !',
                    count:0,
                    items:[]
                }
            }
        }
    </code>
</pre>
### State (State Change)
<pre>
    <code>
        export default{
            data(){
                return{
                    //initial data state
                    message:'Hello Vue !',
                    count:0,
                    items:[]
                }
            },
            methods:{
                //message state change
                changeMessage(){
                    this.message='Vue State Change'
                },
                //count state change
                increment(){
                    this.count++;
                }
            }
        }
    </code>
</pre>

### Virtual DOM
Vue JS က Virtual DOM ကို အသုံးပြုထားတယ်။ Virtual DOM ဆိုတာ Real DOM ရဲ့ Lightweight copy တစ်ခုဖြစ်ပြီး UI changes တွေကို Track လုပ်နေတယ်။ Data တစ်ခုခု change သွားတိုင်းမှာ vue ကနေ Virtual DOM တစ်ခု create လုပ်ပြီး အရင်ရှိနေတဲ့ DOM ရဲ့ ခြားနားချက်ကို Compute လုပ်ပြီး  UI ကို updata လုပ်ပေးတယ်။

### Two Way Data Binding
Vue Js ဟာ UI element နဲ့ Javascript Data Modal တို့ကို အလိုအလျောက် Synchronization ပြုလုပ်ပေးထားတဲ့ two way data binding concept ကို အသုံးပြုထားပါတယ်။ ဆိုလိုတာကတော့ UI element မှာ တစ်ခုခုအပြောင်းအလဲဖြစ်တာနဲ့ Data Modal ကလဲ Update ဖြစ်မှာဖြစ်သလို၊ Data Modal မှာတစ်ခုခုအပြောင်းအလဲဖြစ်တာနဲ့ UI element ကလဲ အလိုအလျှောက် Update ဖြစ်သွားမှာဖြစ်ပါတယ်။

## Vue Components Lifecycle Hooks
#### 1.  Create
    (vue 2)
    1.1 beforeCreated: Executed before the component instance is initialized. Data and events are not set yet.
    1.2 created: Called after the component instance has been created. Data observation, events and computed properties are set yet.

    (vue 3)
    1.1 onBeforeCreate: Called before the component instance is created.
    1.2 onCreated: Called after the component instance is created.
#### 2.  Mount
    (vue 2)
    2.1 beforeMount: Triggered just before the component is inserted into the DOM.
    2.2 mounted: Called once the component is inserted into the DOM. Ideal for initial DOM manipulation and API interactions.

    (vue 3)
    2.1 onBeforeMount: Called before the component is mounted to the DOM.
    2.2 onMounted: Called after the component is mounted.
#### 3.  Update
    (vue 2)
    3.1 beforeUpdate: Called before the component is re-rendered due to data changes. Actions before an update can be performed.
    3.2 updated: Triggered after the component has been re-rendered. Suitable for DOM manipulations that rely on updated data
    (vue 3)
    3.1 onBeforeUpdate: Called before data changes trigger a re-render.
    3.2 onUpdated: called after the component is updated.
#### 4.  Destruction
    (vue 2)
    4.1 beforeDestroy: Called before a component is about to be destroyed. Cleanup tasks such as cancelling timers or event listeners can be done.
    4.2 destroyed: Executed after a component has been destroyed, and all its data and watchers have been cleared.

    (vue 3)
    onBeforeUnmount: Called before the component is unmounted.
    onUnmounted: Called after the component is unmounted.
#### 5. Error Handling
    (vue 2)
    5.1 errorCaptured: Called when an error occurs in any child component or during rendering. Allows capturing and handling errors in the component tree.

    (vue 3)
    5.1 onErrorCaptured: This hook is called when an error is caught in any child component. It's used for error handling and is not a direct equivalent of any Vue 2.x hook.

### Using vue from CDN
HTML page တွေမှာ Vue ကို CDN ကနေအသုံးပြုလိုတဲ့အခါ vue ရဲ့ package ကို HTML page ရဲ့ &lt;script&gt; tag ကနေခေါ်ပြီးအသုံးပြုရမှာဖြစ်ပါတယ်။
#### usage
<pre>
  <code class="language-js" style="margin-left:-140px;">
    &lt;script src="https://unpkg.com/vue@3/dist/vue.global.js"&gt;&lt;/script&gt;
  </code>
</pre>

#### example
#### index.html
<pre>
  <code class="language-html" style="margin-left:-140px;">
    &lt;!DOCTYPE html&gt;
      &lt;html lang="en"&gt;      
      &lt;head&gt;
          &lt;meta charset="UTF-8"&gt;
          &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
          &lt;title&gt; Document&lt;/title&gt;
      &lt;/head&gt;      
      &lt;body&gt;       
          &lt;div id="app"&gt;
              {{count}}
          &lt;/div&gt;
          // from CDN
          &lt;script src="https://unpkg.com/vue@3/dist/vue.global.js"&gt; &lt;/script&gt;
          &lt;script&gt;
              const { createApp } = Vue;
              createApp({
                  data() {
                      return {
                          count: 0
                      }
                  },
              }).mount('#app')
          &lt;/script&gt;
      &lt;/body&gt;       
    &lt;/html&gt;
  </code>
</pre>
အထက်ပါ example မှာဆိုရင် vue ရဲ့ CDN ကို  &lt;script src="https://unpkg.com/vue@3/dist/vue.global.js"&gt; &lt;/script&gt; tag နဲ့ ခေါ်သုံးထားတာဖြစ်ပြီးတော့ ၎င်း CDN ကို HTML page ကနေသိဖို့ဆိုရင်  &lt;script&gt; tag နောက်တစ်ခုကနေ vue ရဲ့ api function ဖြစ်တဲ့ createApp ကို import လုပ်ပေးရမယ်။ အဲ့ဒီ crateApp ကနေ &lt;div&gt; ရဲ့  Id (#app) ကို mount လုပ်ပေးရမှာဖြစ်ပါတယ်။

Vue js ကို Vue SFC Playground Link မှတစ်ဆင့် Test ပြုလုပ်နိုင်ပါတယ်။
[Vue SFC Playground](https://play.vuejs.org/)

#### Attribute Declaration (Variable Declaration)
vue မှာ string၊ integer၊ List အစရှိတဲ့ varablesတွေကို declare လုပ်လိုတဲ့အခါ data function ရဲ့ return value ထဲမှာ declare လုပ်ပေးရမှာဖြစ်ပါတယ်။
#### example
<pre>
  <code class="language-html">              
    data() {
      return {
        message: 'Hello From VUE!',
        count:0,
        list:[],
      }
    },
  </code>
</pre>

## Attribute Binding
vue js မှာ data တွေကို Binding  လုပ်တဲ့အခါ double curly brackets (also called Mustaches) ' {{ }} ' ကိုအသုံးပြုပြီး Bind ရမှာဖြစ်ပါတယ်။

#### example [Vue SFC Playground](https://play.vuejs.org/)

<pre>
  <code class="language-html" style="margin-left:-140px;">    
    //HTML
    &lt;div id="app"&gt;
      {{message}}
    &lt;/div&gt;

    //Script
    &lt;script&gt;         
    data() {
      return {
        message: 'Hello From VUE!'
      }
    },
    &lt;/script&gt;  
  </code>
</pre>

Double Curly Brace ကို HTML Attributes တွေထဲမှာတိုက်ရိုက်အသုံးပြုပြီး Bind လို့မရပါ။ အသုံးပြုလိုပါက v-bind directive ဖြင့်အသုံးပြုရမှာဖြစ်ပါတယ်။
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-html">
    //False
    &lt;div id=" {{id}}"&gt;&lt;/div&gt;  

    //True
    &lt;div v-bind:id="id"&gt;&lt;/div&gt;  
    //short hand
     &lt;div :id="id"&gt;&lt;/div&gt;
  </code>
</pre>

Colon ( : ) နဲ့ စတဲ့ Attribute ဟာ ပုံမှန် HTML attributes ရေးနည်းတွေနဲ့ ကွဲပြားနေပါလိမ့်မယ်။ ဒါပေမယ့် ၎င်း Colon attribute ဟာ vue js ကနေ support ပေးထားတဲ့ valid character attribute ဖြစ်ပြီး Browser က မှန်မှန်ကန်ကန်နဲ့ parse လုပ်ပေးနိုင်ပါတယ်။ Colon ( : )  တစ်နည်းအားဖြင့် Short Hand Syntax ဟာ Vue Developers တွေ ယေဘုလျအသုံးများတဲ့ Syntax တစ်ခုဖြစ်ပါတယ်။
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-html">
    &lt;div :id="id"&gt;&lt;/div&gt;
  </code>
</pre>

## Boolean Attribute
Boolean Attribute ဆိုတာ element တစ်ခုရဲ့ true/false vlaue ကိုညွှန်ပြတဲ့ attribute တစ်ခုဖြစ်ပါတယ်။
Example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-html">
    //true
    &lt;div disabled="true"&gt;&lt;/div&gt;
    //false
    &lt;div disabled="false"&gt;&lt;/div&gt;
  </code>
</pre>
Boolean Attributes တွေကို <code>:disabled</code> ၊ <code>v-if</code> အစရှိတဲ့ condition attributes တွေမှာ အသုံးပြုကြပါတယ်။
#### Example ( <code>:disabled</code> )
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-html">
    &lt;template&gt;
    //button is disabled
      &lt;button :disabled="isDisabled"&gt;Save&lt;/button&gt;
    &lt;/template&gt;
    &lt;script&gt;
      export default{
        data(){
          return{
            isDisabled:true
          }
        }
      }
    &lt;/script&gt;
  </code>
</pre>
#### Example ( <code>v-if</code> )
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-html">
    &lt;template&gt;
      &lt;button v-if="success"&gt;OK&lt;/button&gt;
      &lt;button v-else &gt;Try Again&lt;/button&gt;
    &lt;/template&gt;
    &lt;script&gt;
      export default{
        data(){
          return{
            success:true
          }
        }
      }
    &lt;/script&gt;
  </code>
</pre>

## List Rendering
### v-for
 Vue Js မှာ Arry List တွေကို Render လုပ်တဲ့အခါ <code>v-for</code> directive ကို အသုံးပြုရမှာဖြစ်ပါတယ်။ <code>v-for</code> direvtive မှာဆိုရင် <code>item in items</code> ဆိုတဲ့ Special syntax ကိုအသုံးပြုရမှာဖြစ်ပါတယ်။ <code>items</code>က data array ဖြစ်ပြီး <code>item</code> ကတော့ items array ထဲက alias တစ်ခုဖြစ်ပါတယ်။ <code>v-for</code> directive ဟာ C# Programming Language မှာဆိုရင် for loop လိုမျိုး List ကို Looping ပတ်ခြင်းဖြစ်ပါတယ်။
 #### example
 [Vue SFC Playground](https://play.vuejs.org/)
 <pre>
   <code>
    &lt;template&gt;
      &lt;li v-for="item in items"&gt;
        {{ item.message }}
      &lt;/li&gt;
    &lt;/template&gt;
    &lt;script&gt;
      export default{
       data(){
         return{
           items:[
             {message:'Foo'},{message:'Bar'}
           ]
         }
       }
     }
    &lt;/script&gt;
     //output
     Foo
     Bar
   </code>
 </pre>
<code>v-for</code> directive မှာ item ရဲ့ index ကို သိရှိလိုတဲ့အခါ <code>(item,index) in items</code> ဆိုပြီး အသုံးပြုရမှာဖြစ်ပါတယ်။
#### example
[Vue SFC Playground](https://play.vuejs.org/)
 <pre>
   <code>
    &lt;template&gt;
      &lt;li v-for="(item,index) in items"&gt;
        index:{{ index }} , message: {{item.message}}
      &lt;/li&gt;
    &lt;/template&gt;
    &lt;script&gt;
      export default{
       data(){
         return{
           items:[
             {message:'Foo'},{message:'Bar'}
           ]
         }
       }
     }
    &lt;/script&gt;
     //Output
     index:0, message:Foo
     index:1, message:Bar
   </code>
 </pre>

### <code>v-for</code> with Object
<code>v-for</code> directive မှာ Object တစ်ခုရဲ့  value တင်မဟုတ်ပဲ key ကိုပါ ထပ်ဆင့်ဖော်ပြလိုတဲ့အခါ <code>(value,key,index) in item</code> syntax ကိုအသုံးပြုရမှာဖြစ်ပါတယ်။
ဥပမာ person ဆိုတဲ့ object တစ်ခုမှာ id, name, age ဆိုတဲ့ Fiels တွေပါတယ်ဆိုပါစို့ <code>id</code> က key ဖြစ်ပြီး 1 က value ဖြစ်တယ်။ <code>name</code> က key ဖြစ်ပြီး Alex က value ဖြစ်တယ်။ တစ်နည်းပြောရရင် object တစ်ခုဟာ key,value pair နဲ့ create လုပ်ထားတာဖြစ်တယ်။
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-js">
    const person={
      id:1,
      name:'Alex',
      age:'24'
    }
  </code>
</pre>
object ရဲ့ <code>value</code> မဟုတ်ပဲ <code>key</code> ကိုပါဖော်ပြလိုတယ်ဆိုရင် <code>(value,key,index) in item</code> ဆိုတဲ့ Special Syantax ကို အသုံးပြုရမှာဖြစ်ပါတယ်။
#### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-js">
    //vue template
       &lt;li v-for="(value,key,index) in person"&gt;
        {{ index }} , {{key}}: {{value}}
      &lt;/li&gt;
    //js
    const person={
      id:1,
      name:'Alex',
      age:'24'
    }
    //Output
    0,name:Alex
  </code>
</pre>
#### <code>v-for</code> with <code>v-if</code>
<code>v-if</code> condition directive ကို <code>v-for</code> directive နဲ့သုံးတဲ့အခါမှာ နှစ်မျိုးအသုံးပြုနိုင်တယ်။ တစ်ခုက <code>v-for</code> directive မှာတစ်ခါတည်းသုံးတာရယ်၊ နောက်တစ်ခုက <code>v-for</code> directive သုံးပြီးမှ သုံးတာရယ်။ <code>v-for</code> directive မှာသုံးမယ်ဆိုရင်
<pre>
    <code class="language-vue">
      &lt;li v-for="item in items" v-if="item.success"&gt;
       &lt;span&gt;{{item.message}}&lt;/span&gt;
      &lt;/li&gt;
    </code>
</pre>
ဆိုပြီးသုံးနိုင်တယ်။ <code>v-for</code> directive ပြီးမှ သုံးမယ်ဆိုရင်
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code class="language-vue">
      &lt;li v-for="item in items"&gt;
       &lt;span v-if="item.success"&gt;{{item.message}}&lt;/span&gt;
      &lt;/li&gt;
    </code>
</pre>
ဆိုပြီးသုံးနိုင်တယ်။ အထက်ပါ example နှစ်ခုစလုံးမှာ <code>v-if</code> directive နဲ့စစ်ထားတဲ့ item က success ဖြစ်မှသာ message ကို ပြပေးမှာဖြစ်ပါတယ်။ရေးနည်းပဲကွာပြီး ထွက်လာမယ့် Output ကတော့ အတူတူပါပဲ။

### Maintaining State With <code>key</code>
Vue က 'in-place path' stragegy ကို default အနေဖြင့် အသုံးပြုပြီး element list ကို <code>v-for</code> directive နဲ့ Update လုပ်တယ်။ Data items တွေ changes ဖြစ်သွားတဲ့အခါ အဲ့ဒီ data တွေကို Match လုပ်ဖို့ DOM element ကို ရွှေ့သွားမယ့်အစား Vue က element တွေကို တစ်နေရာတည်းမှာ စုစည်းလိုက်တယ်။ပြီးတော့ ဘယ် element ကတော့ render လုပ်မယ်ဆိုတာကိုဆုံးဖြတ်ပြီး render လုပ်ပေးတယ်။ အဲ့လို default mode နဲ့ အသုံးပြုခြင်းက ကောင်းပေမယ့် temporaty DOM ဟာ child component state အပေါ်မှာမှီခိုနေတဲ့အခါ သုံးရန်မသင့်တော်ပါ။

Node တစ်ခုချင်းစီတိုင်းရဲ့ element identity ကို vue ကနေ track လုပ်ထားပြီး Maintain လုပ်ပေးရမှာဖြစ်တယ်။ အဲ့လို track လုပ်ဖို့ဆိုရင် Unique ဖြစ်တဲ့ <code>key</code> ကိုအသုံးပြုပြီး Maintain လုပ်ပေးရမှာဖြစ်ပါတယ်။
#### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-template">
    &lt;div v-for="item in items" :key="item.id"&gt;
      &lt;!-- content --&gt;
    &lt;/div&gt;
  </code>
</pre>
### <code>v-model</code> directive
<code>v-model</code> directive ဟာ vue ရဲ့ tow way data binding  diretive ဖြစ်ပြီး component တွေရဲ့ date ကို bind တဲ့အခါမှာအသုံးပြုပါတယ်။
data ထဲက declare လုပ်တထား value တွေကို text field သို့မဟုတ် select box ၊ radio button အစရှိတဲ့ element ထဲမှာ <code>v-model</code> directive နဲ့ bind ထားပြီး အဲ့ဒီ text field၊ radio button မှာရှိတဲ့ ui value က changes ဖြစ်သွားရင် data ကလဲ လိုက်ပြီးပြောင်းလဲနေမယ် data က တစ်ခုခု changes ဖြစ်တာနဲ့ text field ၊ select box ၊ radio button စတဲ့ ui element value တွေကလဲ လိုက်ပြီးပြောင်းလဲနေမှာဖြစ်ပါတယ်။
တစ်နည်းအားဖြင့် data မှာ changes ဖြစ်တာနဲ့ UI ကလဲ လိုက်ချိန်းမယ် ၊ UI က value changes ဖြစ်တာနဲ့ data ကလဲသိနေမယ်။
#### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code>
        &lt;template&gt;
          &lt;p&gt;Name : {{name}}&lt;/p&gt;
            &lt;label&gt;Name &lt;input type="text" v-model="name"&gt;&lt;/label&gt;
         &lt;p&gt;Gender : {{gender}}&lt;/p&gt;
              &lt;label&gt;&lt;input type="radio" v-model="gender" v-bind:value="false"&gt;False&lt;/label&gt;
              &lt;label&gt;&lt;input type="radio" v-model="gender" v-bind:value="true"&gt;True&lt;/label&gt;
        &lt;/template&gt;
        
        &lt;script&gt;
            export default{
            data(){
                return{
                    gender:false,
                    name:'Joseph'
                }
            }
        }
        &lt;/script&gt;
    </code>
</pre>
https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/977aaa68-a389-40ca-ac2c-0f01f10b8d65

### <code>v-bind</code> directive
<code>v-bind</code> directive ကို  radio button လိုမျိုး element value တွေကို binding ပြုလုပ်တဲ့အခါမှာအသုံးပြုတယ်။ vue ဟာ element value တွေကို double curley brace နဲ့ binding လုပ်ဖို့ခွင့်မပြုထားပဲ <code>v-bind</code> directive နဲ့သာ binding ပြုလုပ်ဖို့ Support ပေးထားတာဖြစ်ပါတယ်။
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code>
        &lt;template&gt;
         &lt;p&gt;Component Value: {{gender}}&lt;/p&gt;
            &lt;label&gt;&lt;input type="radio" v-model="gender" v-bind:value="false"&gt;False&lt;/label&gt;
            &lt;label&gt;&lt;input type="radio" v-model="gender" v-bind:value="true"&gt;True&lt;/label&gt;
        &lt;/template&gt;
        &lt;script&gt;
            export default{
            data(){
                return{
                    gender:false,
                }
            }
        }
        &lt;/script&gt;
    </code>
</pre>

https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/977aaa68-a389-40ca-ac2c-0f01f10b8d65

### <code>v-on</code> directive
<code>v-on</code> directive ဟာ <code>v-model</code> ၊ <code>v-bind</code> တို့လို vue ရဲ့  build-in directive တစ်ခုဖြစ်ပြီး element တွေရဲ့  click , keypress , enter , prevent အစရှိတဲ့ event တွေကို listen လုပ်တဲ့ directive တစ်ခုဖြစ်ပါတယ်။ပြောရရင် form ကို sumbit လုပ်ဖို့ enter ခလုတ်နှိပ်လို့ရတဲ့ event မျိုး ၊ button ကို  click နှိပ်တာနဲ့ function တစ်ခုကို ခေါ်တာမျိုး textfield ထဲမှာ စာတစ်လုံးရိုက်လိုက်တာနဲ့ ရိုက်လိုက်တဲ့ key က textfield ထဲမှာ မပါစေချင်လို့ pervent လုပ်တဲ့ function ကိုခေါ်ထားတာမျိုးတွေမှာ အသုံးပြုပါတယ်။
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code>
         &lt;template&gt;
           &lt;p&gt;Name : {{name}} &lt;/p&gt;
             &lt;p&gt;Can type Letters Only &lt;/p&gt;
             &lt;label&gt;Name  &lt;input type="text" v-model="name" 
                v-on:keypress="allowLettersOnly($event)" &gt; &lt;/label&gt;
             &lt;p &gt;Enter Key Perss &lt;/p&gt;
             &lt;input type="button" value="Save" v-on:keyup.enter="enterFunc" &gt;
         &lt;/template&gt;
        &lt;script&gt;
            export default{
            data(){
                return{
        
                    gender:true,
                    name:'Joseph'
                }
            },
            methods:{
                allowLettersOnly(e){
                    let char = String.fromCharCode(e.keyCode); // Get the character
                    if (/^[A-Z a-z]+$/.test(char)) return true; // Match with regex 
                    else e.preventDefault(); // If not match, don't add to input text
                },
                enterFunc(){
                    alert('enterkey press')
                }
            }
        }
       &lt;/script&gt;
    </code>
</pre>


https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/1a4532ef-7ac1-440e-a74b-1b6bd5cbd843

<code>v-on</code> direct ကို short-hand နဲ့ရေးမယ်ဆိုရင် <code>@</code> sign နဲ့ရေးနိုင်ပါတယ်။

### Example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code>
        @keypress
        @click
        @keyup.enter
    </code>
</pre>
<pre>
    <code>
         &lt;template&gt;
         &lt;/template&gt;
                &lt;label&gt;Name &lt;input type="text" v-model="name"  @keypress="allowLettersOnly($event)"&gt;&lt;/label&gt;
         &lt;script&gt;
         &lt;/script&gt;
    </code>
</pre>



## API Style
Vue JS မှာ Composition Api နဲ့ Option Api ဆိုပြီး component နှစ်မျိုးရှိပါတယ်။

### Composition API
Compositon API ဆိုတာ vue ရဲ့ API function တွေကို import လုပ်ပြီးအသုံးပြုရတဲ့ Components တွေဖြစ်ပါတယ်။

#### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-js" style="margin-left:-140px;">
    import {ref} from 'vue'  
    import {createApp} from 'vue'
  </code>
</pre>
#### usage
Single File Components (SFCs) တွေမှာဆိုရင် composition api တွေကို &lt;script setup&gt; ထဲမှာရေးသားကြပါတယ်။
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-js" style="margin-left:-140px;">
    <script setup>
      //importing vue api function
        import {ref} from 'vue'  
      //declare count value as 0 by using api function
        const counter=ref(0);     
    </script>
     //vue template
      <template>
        //render count value
        <p>counter value: {{count}}<p>
      </template>
  </code>
</pre>
<code>&lt;script setup&gt;</code> ထဲမှာမရေးပဲ <code>&lt;script&gt;</code> ထဲမှာရေးမယ်ဆိုရင် <code>setup() {}</code> function ထဲမှာ ရေးရမှာဖြစ်ပါတယ်။[Vue SFC Playground](https://play.vuejs.org/)

<pre>
  <code class="language-js" style="margin-left:-140px;">
    &lt;template&gt;
      &lt;h4&gt;Vue Composition API&lt;/h4&gt;
      &lt;p&gt;&#123;&#123; count &#125;&#125; &lt;/p&gt;
    &lt;/template&gt;

    &lt;script&gt;
      import {ref} from 'vue'
      export default{
        setup(){
          const count=ref(0);
          return{
            count,
          }
      }
    &lt;/script&gt;
  </code>
</pre>

[Vue SFC Playground](https://play.vuejs.org/)

<pre>
  <code class="language-js" style="margin-left:-140px;">
    &lt;template&gt;

      &lt;h4&gt;Vue Composition API&lt;/h4&gt;
      &lt;p&gt;&#123;&#123; count &#125;&#125; &lt;/p&gt;
      &lt;button class="btn btn-sm btn-outline-primary me-2" @click="increment"&gt;Increment&lt;/button&gt;
      &lt;button class="btn btn-sm btn-outline-primary me-2" @click="decrement"&gt;Decrement&lt;/button&gt;

    &lt;/template&gt;

    &lt;script&gt;
      import {ref} from 'vue'
      export default &#123;
        name: 'CounterApp'
        setup()&#123;
          const count=ref(0);
          //increment function of count
          function increment(){
            this.count++;
          }
          //decrement function of count
          function decrement(){
            this.count--;
          }
          //data and function must return for tracking state change
          return{
            count,
            increment,
            decrement
          }
        &#125;
      &#125;
    &lt;/script&gt;
  </code>
</pre>


https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/935ad281-da4e-463f-8e60-1ed557c8fb0b


### Option API
<code>data</code>၊ <code>methods</code>၊ <code>mounted</code> အစရှိတဲ့ Object တစ်ခုရဲ့ Option API တွေကိုအသုံးပြုပြီး Component Logic တွေကို Define ပြုလုပ်နိုင်ပါတယ်၊ Option တွေကနေ Define လုပ်ထားတဲ့ properties တွေကို function တွေကနေ <code>this</code> keyword ကိုသုံးပြီး ပြန်လည်အသုံးပြုရမှာဖြစ်ပါတယ်။

### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-template">
      &lt;template&gt;
        &lt;p&gt;{{message}}&lt;/p&gt;
      &lt;/template&gt;
      &lt;script&gt;
          export default &#123;
            data(){
              return{
                message:'Vue JS !'
              }
            },
            mounted(){
              console.log(this.message);
            }
          &#125;
      &lt;/script&gt;
  </code>
</pre>


https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/cb1e4d2e-cb0d-46ee-8861-86c14238d05a

## <code>v-model</code>
Option Api ထဲက fuction တွေအကြောင်းမပြောခင်မှာ tow way data binding ကို implement လုပ်ပေးတဲ့ <code>v-model</code> directive အကြောင်းကို ပထမဆုံးသိထားရမယ်။  <code>v-model</code> ဆိုတာ Form input value၊ option value အစရှိတဲ့ input element တွေနဲ့ component data တွေကြားကို binding လုပ်ပေးတဲ့ directive တစ်ခုပဲဖြစ်တယ်။
### 1. Data Binding
Vue components မှာ component data ကို input element ထဲမှာ Bind တဲ့အခါ <code>v-model</code> directive ကို အသုံးပြုပြီး Binding လုပ်ပေးရတယ်။
### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code class="language-template">
        &lt;template&gt;
            &lt;input type="text" v-model="message"&gt;
        &lt;/template&gt;
    </code>
</pre>
### 2. Two Way Binding
<code>v-model</code> directive က input element မှာတစ်ခုခု အပြောင်းအလဲဖြစ်တာနဲ့ component data ကိုလဲ အလိုအလျှောက်ပြောင်းလဲပေးပြီး component data က တစ်ခုခုအပြောင်းအလဲဖြစ်တာနဲ့ input element ကို Update လုပ်ပေးတဲ့ tow way data binding directive တစ်ခုဖြစ်တယ်။
### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code class="language-template">
        &lt;template&gt;
            &lt;p&gt;{{message}}&lt;/p&gt;
            &lt;input type="text" v-model="message"&gt;
        &lt;/template&gt;
        &lt;script&gt;
            export default{
                data(){
                    return{
                        message:'Two Way Binding'
                    }        
                }
            }
        &lt;/script&gt;
    </code>
</pre>



https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/92bba612-1b8c-45c7-a251-5132cfdc25ba



### Created
Created က component instance တွေ create လုပ်ပြီးတဲ့အခါ စပြီးအလုပ်လုပ်တယ်။
### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-template">
      &lt;template&gt;
        &lt;p&gt;{{message}}&lt;/p&gt;
      &lt;/template&gt;
      &lt;script&gt;
          export default &#123;
            data(){
              return{
                message:'Vue JS !'
              }
            },
            created(){
              this.message="Vue JS application"
              console.log(this.message);
            }
          &#125;
      &lt;/script&gt;
  </code>
</pre>
အထက်ပါ example မှာဆိုရင် output က <code>Vue JS application</code> ဆိုပြီးထွက်မယ်။ data function ရဲ့ return value ထဲမှာ message ကို <code>Vue JS !</code> လို့ assign လုပ်ထားတယ်ဆိုပေမယ့် message က component တွေ create မလုပ်ပြီးခင်မှာပဲ  <code>Vue JS !</code> လို့ရှိနေပြီး component တွေ create လုပ်ပြီးသွားတဲ့အခါ created function ထဲကိုရောက်သွားတယ်။ အဲ့ဒီ created ထဲမှာ <code>this.message="Vue JS application"</code> ဆိုပြီး assign လုပ်လိုက်တဲ့အတွက်ကြောင့် message ဟာ <code>Vue JS application</code> ဖြစ်သွားပြီး UI ကို update လုပ်ပေးလိုက်တယ်။



https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/e2e6b6cf-0f72-4871-9b94-14dc5ddf2871



### Mounted
Mounted  က component တွေကို DOM ထဲထည့်ပြီးတဲ့အချိန်မှ  စပြီးအလုပ်လုပ်တယ်။
### example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
  <code class="language-template">
      &lt;template&gt;
        &lt;p&gt;{{message}}&lt;/p&gt;
      &lt;/template&gt;
      &lt;script&gt;
          export default &#123;
            data(){
              return{
                message:'Vue JS !'
              }
            },
            created(){
              this.message="Vue JS application created"
              console.log(this.message);
            },
            mounted(){
              this.message="Vue JS application mounted"
              console.log(this.message);
            }
          &#125;
      &lt;/script&gt;
  </code>
</pre>
အထက်ပါ example မှာဆိုရင် ပထမဆုံး data ထဲမှာ message က <code>Vue JS !</code>  ဆိုပြီး assign လုပ်ထားတယ်။ Component တွေကို initialize လုပ်ပြီးတဲ့အချိန်မှာ created function ထဲကိုရောက်သွားပြီး အဲ့ဒီ function ထဲမှာ <code>this.message="Vue JS application created"</code> ဆိုပြီး message ကို assign ပြန်လုပ်လိုက်တဲ့အတွက်ကြောင့် message က <code>Vue JS application created</code> ဆိုပြီးဖြစ်သွားမယ်။ created function အလုပ်လုပ်ပြီးသွားတဲ့အခါ vue က component တွေကို DOM ထဲထည့်လိုက်ပြီးတော့ mounted function ကစပြီးအလုပ်လုပ်ပြီ။ mounted ထဲမှာ <code>this.message="Vue JS application mounted"</code> ဆိုပြီး assign လုပ်လိုက်တဲ့အတွက်ကြောင့် message ရဲ့ data change သွားပြီးတော့ virtual dom ကနေ UI ကို <code>Vue JS application mounted</code> update သွားလုပ်ပေးလိုက်တယ်။



https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/b429d33a-5cf5-4ddf-8f11-a5cac5c23534

### updated 
Vue မှာ data state တွေကို track လုပ်နေပြီးတော့ state တစ်ခုခုပြောင်းသွားတိုင်းမှာ updated ကသိနေမယ်။
ဥပမာ template ထဲမှာ number input box တစ်ခုရှိမယ် ‌အဲ့ဒီ nuber text box ရဲ့ ကို v-model directive နဲ့ count value ကို Bind ထားမယ်ပေါ့။ script ရဲ့ data ထဲမှာတော့ count value ကို 1 လို့ declare လုပ်ထားပြီး return ပြန်ထားမယ်။ အဲ့မှာ number box မှာ count value ပြောင်းတာနဲ့ data ရဲ့ count value ကလဲ two way data binding ကြောင့်ပြောင်းသွားမယ်။ အဲ့လိုပြောင်းသွားတာကို vue ရဲ့ တစ်ခြား component ကနေသိလိုတာဖြစ်ဖြစ် ကိုယ်တိုင်က အဲ့လိုပြောင်းလဲတဲ့အပေါ်မူတည်ပြီး function တစ်ခုခုကို အလုပ်လုပ်စေလိုတဲ့အခါ updated function ထဲမှာ ရေးရမှာဖြစ်တယ်။
### Example
[Vue SFC Playground](https://play.vuejs.org/)
<pre>
    <code>
        &lt;template&gt;
          &lt;label&gt;number &lt;input type="number" v-model="count"&gt;&lt;/label&gt;
        &lt;/template&gt;
        &lt;script&gt;
          export default{
            data(){
              return{
                count:0
              }
            },
            updated(){
              alert(this.count)
            }
          }
        &lt;/script&gt;    
    </code>
</pre>

https://github.com/mmcodetester/vue-basic-myanmar-version/assets/72187529/9f39f06a-da8b-4880-9fd3-6850b512327f

## Props
## Event
## Keep Alive
<code>KeepAlive</code> 

