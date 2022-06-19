```typescript
import YandexPracticum from 'https://practicum.yandex.ru/web/';

type Work = {
  companyName: string;
  description: string;
  hardSkills: string[];
  work(backlog?: {}): {};
};

class WebDeveloper extends YandexPracticum {

    private name;
    private age;
    private location;
    public motivation;
    public myWork: Work | undefined | null;

  constructor(name: string, age: number, location: string, motivation: string[], hardSkills?: string[]) {
    super(hardSkills);
    this.name = name;
    this.age = age;
    this.location = location;
    this.motivation = motivation;
  }

  public getWork(someSite: Work[]): void {
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
    
    this.myWork = someSite.find(vacancy => vacancy.hardSkills === this.hardSkills);
  }
  
  public getMotivation() {
    console.log(this.motivation);
  }
  
  public doWork() {
    this.getMotivation();
    this.myWork.work();
  }
  
  public learn(newHardSkills: string) {
    this.hardSkills.push(newHardSkills);
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
