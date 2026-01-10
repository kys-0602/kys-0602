```ts
type Project = {
  desc: string;
  link: string;
  role: string[];
  techStack: string[];
  teamMembers: string[] | null;
};

class Profile {
  location             : string;
  programmingLanguages : string[];
  markupLanguages      : string[];
  frameworks           : string[];
  databases            : string[];
  tools                : string[];
  currentlyLearning    : string[];
  education            : { ssafy: { desc: string; achievement: string[] } };
  projects             : Record<string, Project>;
  contact              : { email: string; blog: string };

  constructor() {
    this.location = "Seoul, South Korea";

    this.programmingLanguages  = [ "C", "C++", "Java", "JavaScript", "TypeScript" ];
    this.markupLanguages       = [ "HTML", "CSS", "Markdown" ];
    this.frameworks            = [ "Node.js", "Vue", "Vite" ];
    this.databases             = [ "MySQL", "MariaDB", "SQLite" ];
    this.tools                 = [ "Git", "VSCode", "Postman", "Figma", "IntelliJ", "Notion" ];

    this.currentlyLearning     = [ "Algorithm & Problem Solving", "Vue", "React", "Node.js" ];

    this.education = {
      ssafy: {
        desc        : "14th, Seoul Campus, Java & Web Track",
        achievement : [ "Classmate of the Month", "Class President, Class 2, Semester 2" ]
      }
    };

    this.projects = {
      yumgovy: {
        desc      : "AI-based Diet Coaching",
        link      : "https://github.com/kys-0602/yumgovy-fe",
        role      : [ "Front-End", "Teammate" ],
        techStack : [ "Vue", "TailwindCSS" ],
        teamMembers: [  ],
      },

      sywworkshop: {
        desc      : "SPR/YTL/YAV/PAL Viewer",
        link      : "https://syw-kr.github.io/workshop/",
        role      : [ "Front-End", "Owner(Personal)" ],
        techStack : [ "Vue", "TailwindCSS" ],
        teamMembers: null,
      },

      CollaborativePJT: {
        desc      : "SSAFY 14th, Second Semester CollaborativePJT",
        link      : "",
        role      : [ "Front-End", "Team Leader" ],
        techStack : [ ], 
        teamMembers: [  ],
      }
    };

    this.contact = {
      email : "i.am.happy.kr@gmail.com",
      blog  : "https://kys-0602.github.io/"
    };
  }

  introduce = (): string => {
    return `저는 ${this.location}에 위치한, Front-End 개발자를 꿈꾸는 사람입니다. 현재 ${this.currentlyLearning.join(", ")}를 배우고 있어요.`;
  };
}

const me = new Profile();
console.log(me.introduce());
```
![snake animation](https://raw.githubusercontent.com/kys-0602/kys-0602/output/github-contribution-grid-snake.svg)
