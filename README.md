```javascript
import YandexPracticum from 'https://practicum.yandex.ru/web/';

class WebDeveloper extends YandexPracticum {

  constructor(hardSkills, name, age, location, motivation) {
    super(hardSkills);
    this._name = name;
    this._age = age;
    this._location = location;
    this._motivation = motivation;
    this._myWork = null;
  }

  getWork(someSite) {
    console.log(this.hardSkills);
    // [object Array] (9)
    [
       'HTML',
       'CSS',
       'JavaScript',
       'React',
       'Express.js',
       'БЭМ',
       'GIT',
       'MongoDB',
       'Webpack'
    ]
    
    this._myWork = someSite.find(vacancy => vacancy.hardSkills === this.hardSkills);
  }
  
  getMotivation() {
    console.log(this._motivation);
  }
  
  doWork() {
    this.getMotivation();
    this._myWork.work();
  }
  
  learn(newHardSkills) {
    this.hardSkills.push(newHardSkills);
  }
  
  goToSleep() {
    setTimeout(wakeUp, 28800000);
  }
  
};

const zoytz = new WebDeveloper('Алексей', 33, 'Москва', ['Еда', 'Путь к Middle web-developer']);

zoytz.learn('TypeScript');
zoytz.getWork(https://hh.ru/);
```

<!--
**Zoytz/Zoytz** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
