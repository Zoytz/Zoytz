```javascript
import YandexPracticum from 'https://practicum.yandex.ru/web/';
import HeadHunterRu from 'https://hh.ru';

console.log(YandexPracticum.hardSkills);
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

class WebDeveloper extends YandexPracticum {

  constructor(name, age, location, motivation, hardSkills) {
    super(hardSkills);
    this.name = name;
    this.age = age;
    this.location = location;
    this.motivation = motivation;
  }

  getWork(someSite) {
    this.myWork = someSite.find(vacancy => vacancy.hardSkills === this.hardSkills);
  }

  learn(newHardSkills) {
    this.hardSkills.push(newHardSkills);
  }
  
};

const zoytz = new WebDeveloper('Алексей', 34, 'Москва', ['Еда', 'Путь к Middle web-developer']);

zoytz.learn('TypeScript');
zoytz.learn('Next.js');
zoytz.learn('Styled Components');
zoytz.learn('Less');
zoytz.learn('Redux Toolkit');
        
zoytz.getWork(HeadHunterRu);
```
