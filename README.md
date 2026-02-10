```ts
type Project = {
  title: string;
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
    this.location = "Seongnam-si, Gyeonggi-do, Republic of Korea";

    this.programmingLanguages  = [ "C", "C++", "Java", "JavaScript", "TypeScript" ];
    this.markupLanguages       = [ "HTML", "CSS", "Markdown" ];
    this.frameworks            = [ "Node.js", "Vue", "Vite" ];
    this.databases             = [ "MySQL", "MariaDB", "SQLite" ];
    this.tools                 = [ "Git", "VSCode", "Postman", "Figma", "IntelliJ", "Notion" ];

    this.currentlyLearning     = [ "Algorithm & Problem Solving", "Vue", "React", "Node.js" ];

    this.education = {
      ssafy: {
        desc        : "14th, Seoul Campus, Java & Web Track",
        achievement : [ "Classmate of the Month", "Class President, Class 2, Semester 2", "CommonPJT BestMember" ]
      }
    };

    this.projects = {
      yumgovy: {
        title     : "YumGovy",
        desc      : "AI-based Diet Coaching",
        link      : "https://github.com/kys-0602/yumgovy-fe",
        role      : [ "Front-End", "Teammate" ],
        techStack : [ "Vue", "TailwindCSS" ],
        teamMembers: [  ],
      },

      sywworkshop: {
        title     : "SYWWorkShop",
        desc      : "SPR/YTL/YAV/PAL Viewer",
        link      : "https://syw-kr.github.io/workshop/",
        role      : [ "Front-End", "Owner(Personal)" ],
        techStack : [ "Vue", "TailwindCSS" ],
        teamMembers: null,
      },

      CollaborativePJT: {
        title     : "RoomInCode"
        desc      : "실시간 턴제 코딩 배틀 게임",
        link      : "",
        role      : [ "Front-End", "Team Leader" ],
        techStack : [ "Vue.JS", "TypeScript", "TailwindCSS", "Naive UI", "Axios", "MonacoEditor", "Yjs", "WebSocket(RAW)" ], 
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
