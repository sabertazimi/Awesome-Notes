# Library Basic Notes

<!-- TOC -->

- [Library Basic Notes](#library-basic-notes)
  - [Indexing Tools](#indexing-tools)
  - [Boilerplate](#boilerplate)
  - [UI Framework](#ui-framework)
  - [Framework and Solution](#framework-and-solution)
    - [Frontend Solution](#frontend-solution)
    - [Micro Frontends Solution](#micro-frontends-solution)
    - [Backend Solution](#backend-solution)
    - [Full Stack Solution](#full-stack-solution)
    - [Desktop Solution](#desktop-solution)
  - [State Data Management](#state-data-management)
    - [Redux](#redux)
    - [Hooks](#hooks)
    - [Other](#other)
  - [Browser Utils](#browser-utils)
  - [JavaScript Utils](#javascript-utils)
    - [String Utils](#string-utils)
    - [Functional Programming Utils](#functional-programming-utils)
    - [TypeScript Utils](#typescript-utils)
  - [CSS Utils](#css-utils)
    - [Color Utils](#color-utils)
    - [Gradients Utils](#gradients-utils)
    - [Box Shadows Utils](#box-shadows-utils)
    - [Background Utils](#background-utils)
  - [Components](#components)
    - [Layout](#layout)
    - [Navigation](#navigation)
    - [Landing Page](#landing-page)
    - [Button](#button)
    - [Card](#card)
    - [Chat Widgets](#chat-widgets)
    - [Comments System](#comments-system)
    - [Message](#message)
      - [Page Indicator](#page-indicator)
      - [Prompt](#prompt)
      - [Alert](#alert)
      - [Focus](#focus)
      - [Tooltip](#tooltip)
    - [Form](#form)
      - [Input](#input)
      - [Select](#select)
      - [Validator](#validator)
    - [List](#list)
      - [List Virtualized Windowing](#list-virtualized-windowing)
    - [Table](#table)
    - [Charts](#charts)
    - [Slides](#slides)
    - [iFrame](#iframe)
  - [Viewport Utils](#viewport-utils)
    - [Scroll Utils](#scroll-utils)
    - [Mouse Utils](#mouse-utils)
  - [Animation](#animation)
    - [Typing Effect Animation](#typing-effect-animation)
    - [Loading Effect Animation](#loading-effect-animation)
      - [Progress Bar](#progress-bar)
      - [Skeleton](#skeleton)
      - [Spinner](#spinner)
    - [Hover Effect Animation](#hover-effect-animation)
  - [Time](#time)
    - [Date](#date)
    - [Calendar](#calendar)
  - [i18n](#i18n)
  - [Social Sharing](#social-sharing)
  - [Fonts](#fonts)
  - [Images](#images)
    - [Image Color](#image-color)
    - [Icons](#icons)
    - [Emoji](#emoji)
    - [SVG](#svg)
    - [Image Size](#image-size)
    - [Slide Images](#slide-images)
    - [Image Gallery](#image-gallery)
    - [Image Filter](#image-filter)
  - [Canvas](#canvas)
    - [Particles](#particles)
    - [Blocks](#blocks)
    - [3D Engine](#3d-engine)
  - [Media](#media)
    - [Audio](#audio)
    - [Video](#video)
  - [Clipboard](#clipboard)
  - [Keyboard](#keyboard)
  - [Editor](#editor)
    - [Rich Text Editor](#rich-text-editor)
    - [Code Editor](#code-editor)
  - [SMS](#sms)
    - [Phone](#phone)
    - [Email](#email)
  - [File](#file)
    - [File Uploader](#file-uploader)
    - [File Downloader](#file-downloader)
    - [File Utils](#file-utils)
    - [PDF](#pdf)
  - [Persistent Storage](#persistent-storage)
  - [Search](#search)
  - [CLI](#cli)
    - [CLI Compiler](#cli-compiler)
    - [CLI Library](#cli-library)
    - [Terminal](#terminal)
  - [Daemon](#daemon)
  - [Network](#network)
    - [Network Protocols](#network-protocols)
    - [Web Socket](#web-socket)
    - [P2P](#p2p)
    - [Pre-Fetch](#pre-fetch)
    - [Lazy Loading](#lazy-loading)
    - [Network Benchmark](#network-benchmark)
    - [Network Debugging](#network-debugging)
  - [Server](#server)
    - [Serverless](#serverless)
  - [Encryption](#encryption)
  - [Debug Testing](#debug-testing)
    - [Unit Testing](#unit-testing)
    - [Feature Testing](#feature-testing)
    - [End to End Testing](#end-to-end-testing)
    - [Headless Web Tools](#headless-web-tools)
    - [Code Analysis Tools](#code-analysis-tools)
    - [Code Coverage Tools](#code-coverage-tools)
    - [Code Quality Tools](#code-quality-tools)
    - [Inspect Tools](#inspect-tools)
    - [Monitoring Tools](#monitoring-tools)
    - [Performance Tools](#performance-tools)
    - [Log Tools](#log-tools)
    - [Mock Tools](#mock-tools)
    - [Security Tools](#security-tools)
    - [UML Tools](#uml-tools)
  - [DevOps](#devops)
    - [Project Tools](#project-tools)
    - [CI Tools](#ci-tools)
  - [Documentation](#documentation)

<!-- /TOC -->

## Indexing Tools

- [Open Base](https://openbase.com)
- [Best of JS](https://github.com/bestofjs/bestofjs-webui)
- [Micro.js](https://github.com/microjs/microjs.com)
- [NPM Package Trends](https://github.com/johnmpotter/npm-trends)
- [NPM Package Cost](https://github.com/pastelsky/bundlephobia)

## Boilerplate

- [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate)
- [Create React App](https://github.com/facebook/create-react-app)
- [React Component Boilerplate](https://github.com/insin/nwb)
- [Neutrino.js Customizable Boilerplate](https://github.com/neutrinojs/neutrino)
- [Hygen Component Generator](https://github.com/jondot/hygen)
- [React Chrome Extension](https://github.com/FullStack-Academy-Kiev/react-chrome-extension)
- [Vue CLI](https://github.com/vuejs/vue-cli)
- [Vite](https://github.com/vitejs/vite)

## UI Framework

- [React Ant Design](https://github.com/ant-design/ant-design)
- [React Mantine with Hooks](https://github.com/mantinedev/mantine)
- [React Material UI](https://github.com/mui-org/material-ui)
- [React Semantic UI](https://github.com/Semantic-Org/Semantic-UI-React)
- [React BluePrint](https://github.com/palantir/blueprint)
- [IceWorks](https://alibaba.github.io/ice/iceworks)
- [Vue Admin UI](https://github.com/epicmaxco/vuestic-admin)
- [Tailwind](https://github.com/tailwindlabs/tailwindcss)
- [Bootstrap](https://github.com/twbs/bootstrap)
- [Paper.css](https://github.com/papercss/papercss)
- [NES.css](https://github.com/nostalgic-css/NES.css)

## Framework and Solution

### Frontend Solution

- [React Storybook](https://github.com/storybooks/storybook)
- [Gatsby.js](https://github.com/gatsbyjs/gatsby)
- [UMI](https://github.com/umijs/umi)

### Micro Frontends Solution

- [Bit](https://github.com/teambit/bit)
- [UMI QianKun](https://github.com/umijs/qiankun)
- [IceStark](https://github.com/ice-lab/icestark)
- [Single SPA](https://github.com/single-spa/single-spa)

### Backend Solution

- [Egg.js](https://github.com/eggjs/egg)
- [Feathers.js: RESTful API](https://github.com/feathersjs/feathers)

### Full Stack Solution

- [Next.js](https://github.com/zeit/next.js)

### Desktop Solution

- [Electron](https://github.com/electron/electron)
- [Tauri](https://github.com/tauri-apps/tauri)

## State Data Management

### Redux

- [Redux Helper Tools](https://github.com/reduxjs/redux-starter-kit)
- [Reselect](https://github.com/reactjs/reselect)

### Hooks

- [React Hooks Gallery](https://nikgraf.github.io/react-hooks)
- [Ali Hooks](https://github.com/alibaba/hooks)

### Other

- [RxJS Middleware](https://github.com/redux-observable/redux-observable)
- [React Resolver](https://github.com/ericclemmons/react-resolver)
- [Baobab](https://github.com/Yomguithereal/baobab)

## Browser Utils

- [Browser Platform Detection](https://github.com/lancedikson/bowser)
- [Browser Feature Detection](https://github.com/Modernizr/Modernizr)

## JavaScript Utils

- [Cash: jQuery Lite](https://github.com/kenwheeler/cash)

### String Utils

- [String Manipulation](https://github.com/dleitee/strman)
- [Fuzzy String Matching](https://github.com/nol13/fuzzball.js)

### Functional Programming Utils

- [Immer](https://github.com/immerjs/immer)

### TypeScript Utils

- [TypeBox: JSON Schema Type Builder](https://github.com/sinclairzx81/typebox)

## CSS Utils

- [CSS Normalize](https://github.com/necolas/normalize.css)
- [Styled System](https://github.com/styled-system/styled-system)
- [CSS Classnames](https://github.com/JedWatson/classnames)
- [Awesome Design Tools](https://github.com/LisaDziuba/Awesome-Design-Tools)

### Color Utils

- [Color Palettes from Online Website](https://github.com/cloudflare-design/color)
- [Culori](https://github.com/Evercoder/culori)
- [Color Difference Library](https://github.com/lokesh/color-thief)

### Gradients Utils

- [Web Gradients](https://webgradients.com)

### Box Shadows Utils

- [Box Shadows](https://madeas.github.io/box-shadows)

### Background Utils

- [Clippy: Clip-Path Maker](https://github.com/bennettfeely/Clippy)

## Components

### Layout

- [Full Page Layout](https://github.com/alvarotrigo/fullPage.js)
- [One Page Layout](https://github.com/davist11/jQuery-One-Page-Nav)
- [React Panel Group](https://github.com/DanFessler/react-panelgroup)
- [Bricks Layout](https://github.com/callmecavs/bricks.js)
- [Brick Layer](https://github.com/ademilter/bricklayer)
- [Tether: Element Location](https://github.com/HubSpot/tether)
- [SplitJS](https://github.com/nathancahill/Split.js)

### Navigation

- [Okay nav](https://github.com/VPenkov/okayNav)
- [Animated Nav Burgers](https://github.com/march08/animated-burgers)
- [Menu Icon Click Animation](https://github.com/jonsuh/hamburgers)
- [Pagemap](https://github.com/lrsjng/pagemap)

### Landing Page

- [Video Landing Page](https://github.com/rishabhp/bideo.js)

### Button

- [React Awesome 3D Button](https://github.com/rcaferati/react-awesome-button)
- [Tiny Fab](https://github.com/dericgw/react-tiny-fab)

### Card

- [GitHub Information Card](https://github.com/lepture/github-cards)
- [Bootcards](https://github.com/bootcards/bootcards)

### Chat Widgets

- [React Chat Widget](https://github.com/Wolox/react-chat-widget)
- [Matrix](https://github.com/matrix-org/matrix-react-sdk)
- [JsSIP: Chat Library](https://github.com/versatica/JsSIP)

### Comments System

- [Utterances: GitHub Issue Based Comments Widget](https://github.com/utterance/utterances)
- [Disqus](https://github.com/disqus/disqus-react)

### Message

- [Awesome Prompt Messenger](https://github.com/HubSpot/messenger)
- [TheaterJS: Typing Effect](https://github.com/Zhouzi/TheaterJS)
- [Guide Tour](https://github.com/shipshapecode/shepherd)
- [Intro.js](https://github.com/usablica/intro.js)

#### Page Indicator

- [React Snakke](https://github.com/diogomoretti/react-snakke)

#### Prompt

- [GalGame ChatView](https://github.com/webcyou/MessageViewJS)
- [Popper.js](https://github.com/FezVrasta/popper.js)
- [Humane.js](https://github.com/wavded/humane-js)
- [Desktop Notification](https://github.com/Nickersoft/push.js)
- [Nodejs Notification](https://github.com/mikaelbr/node-notifier)

#### Alert

- [Sweet Alert 2](https://github.com/sweetalert2/sweetalert2)
- [Sweet Alert](https://github.com/t4t5/sweetalert)

#### Focus

- [driver.js](https://github.com/kamranahmedse/driver.js)

#### Tooltip

- [tippy.js](https://github.com/atomiks/tippyjs)
- [Balloon Hovering Tooltips](https://github.com/kazzkiq/balloon.css)
- [Hint.css Tooltips](https://github.com/chinchang/hint.css)
- [React Tooltip](https://github.com/tvkhoa/react-tippy)

### Form

- [React Formik](https://github.com/jaredpalmer/formik)
- [Form Boilerplate](https://github.com/andybelldesign/boilerform)

#### Input

- [IMask.js: Input Mask](https://github.com/uNmAnNeR/imaskjs)
- [Super Placeholder](https://github.com/chinchang/superplaceholder.js)
- [AutoComplete.js](https://github.com/TarekRaafat/autoComplete.js)

#### Select

- [React Select](https://github.com/JedWatson/react-select)
- [Select.css](https://github.com/filamentgroup/select-css)
- [Awesome Chosen](https://github.com/harvesthq/chosen)

#### Validator

- [Promise Validator](https://github.com/poppinss/indicative)
- [Async Validator](https://github.com/yiminghe/async-validator)
- [Input Format](https://github.com/nosir/cleave.js)
- [joi](https://github.com/hapijs/joi)
- [yup](https://github.com/jquense/yup)
- [jQuery Form Validator](https://github.com/victorjonsson/jQuery-Form-Validator)

### List

- [Sortable](https://github.com/RubaXa/Sortable)

#### List Virtualized Windowing

- [React Virtualized- Original Component](https://github.com/bvaughn/react-virtualized)
- [React Virtualized Auto Sizer](https://github.com/bvaughn/react-virtualized-auto-sizer)
- [React Window: Brand New React Virtualized](https://github.com/bvaughn/react-window)
- [React Virtuoso](https://github.com/petyosi/react-virtuoso)
- [Vue Virtual Scroller](https://github.com/Akryum/vue-virtual-scroller)

### Table

- [React Table(with Hooks API)](https://github.com/tannerlinsley/react-table)
- [React Datasheet](https://github.com/nadbm/react-datasheet)
- [Bootstrap Table](https://github.com/wenzhixin/bootstrap-table)

### Charts

- [React Chartjs](https://github.com/jhudson8/react-chartjs)
- [Sigma.js: Graph Drawing](https://github.com/jacomyal/sigma.js)
- [HTML5 Chart](https://github.com/chartjs/Chart.js)
- [Plotly.js](https://github.com/plotly/plotly.js)

### Slides

- [MDX Deck](https://github.com/jxnblk/mdx-deck)
- [React Spectacle](https://github.com/FormidableLabs/spectacle)
- [Reveal.js HTML Presentation](https://github.com/hakimel/reveal.js)
- [Glider.js](https://github.com/NickPiscitelli/Glider.js)
- [CLI Animation Presentation](https://github.com/neatsoftware/term-sheets)
- [Awesome Prezi-Like Presentation](https://github.com/impress/impress.js)
- [Awesome Slide Gallery](https://github.com/kenwheeler/slick)
- [One Page Vertical Slide](https://github.com/MopTym/doSlide)

### iFrame

- [Postmate](https://github.com/dollarshaveclub/postmate)

## Viewport Utils

- [Viewport Events](https://github.com/robb0wen/tornis)
- [Robot.js: Node.js Desktop Automation](https://github.com/octalmage/robotjs)

### Scroll Utils

- [Scroll Reveal](https://github.com/jlmakes/scrollreveal)
- [AOS Scroll Animation](https://github.com/michalsnik/aos)
- [Lax Scroll Animation](https://github.com/alexfoxy/laxxx)
- [Scroll Bar Detection](https://github.com/idiotWu/smooth-scrollbar)

### Mouse Utils

- [React Draft.js](https://github.com/draft-js-plugins/draft-js-plugins)
- [React Beautiful DnD](https://github.com/atlassian/react-beautiful-dnd)
- [React DnD: Drag and Drop](https://github.com/react-dnd/react-dnd)
- [Moveable](https://github.com/daybrush/moveable)
- [P5.js](https://github.com/processing/p5.js)
- [Nipple.js](https://github.com/yoannmoinet/nipplejs)
- [Interact.js: Drag, Drop and Resizing Multi Touch](https://github.com/taye/interact.js)
- [Drag and Drop Grid Layout](https://github.com/jbaysolutions/vue-grid-layout)
- [Moveable](https://github.com/daybrush/moveable)

## Animation

- [React Spring](https://github.com/react-spring/react-spring)
- [Framer Motion](https://github.com/framer/motion)
- [React Transition Group](https://github.com/reactjs/react-transition-group)
- [React Animation](https://github.com/FunctionFoundry/react-set-animate)
- [GreenSock](https://github.com/greensock/GreenSock-JS)
- [Airbnb AE Solution](https://github.com/airbnb/lottie-web)
- [Effeckt.css](https://github.com/h5bp/Effeckt.css)
- [animate.css](https://github.com/daneden/animate.css)
- [Anime](https://github.com/juliangarnier/anime)
- [Velocity Animation](https://github.com/julianshapiro/velocity)
- [Ramjet](https://github.com/rich-harris/ramjet)
- [Barba.js](https://github.com/luruke/barba.js)
- [Motto Animated Words](https://github.com/jrainlau/motto)
- [Popmotion](https://github.com/popmotion/popmotion)

### Typing Effect Animation

- [Typed.js](https://github.com/mattboldt/typed.js)
- [TypeIt](https://github.com/alexmacarthur/typeit)

### Loading Effect Animation

#### Progress Bar

- [NProgress.js](https://github.com/rstacruz/nprogress)

#### Skeleton

- [Vue Skeleton](https://github.com/egoist/vue-content-loader)

#### Spinner

- [Epic Spinners](https://github.com/epicmaxco/epic-spinners)
- [Loading IO](https://loading.io)

### Hover Effect Animation

- [Image Hover](http://imagehover.io)
- [Hovering Button Effects](https://github.com/IanLunn/Hover)

## Time

### Date

- [Day.js](https://github.com/iamkun/dayjs)
- [Date Lodash](https://github.com/date-fns/date-fns)
- [Moment.js](https://github.com/moment/moment)
- [Time Table](https://github.com/flightplan-tool/timetable-fns)

### Calendar

- [Big Calendar](https://github.com/intljusticemission/react-big-calendar)
- [React Calendar](https://github.com/moodydev/react-calendar)
- [GitHub Style Calendar](https://github.com/DKirwan/calendar-heatmap)

## i18n

- [React i18n Next](https://github.com/i18next/react-i18next)
- [React Intl](https://github.com/formatjs/formatjs)
- [Numbers and Currencies](https://github.com/autoNumeric/autoNumeric)

## Social Sharing

- [One-Key Share](https://github.com/overtrue/share.js)
- [Sharing](https://github.com/mxstbr/sharing)
- [Social Share URLs](https://github.com/bradvin/social-share-urls)

## Fonts

- [Fontmin](https://github.com/ecomfe/fontmin)
- [Chinese WebFont Zip](https://github.com/aui/font-spider)
- [Fonts.css](https://github.com/zenozeng/fonts.css)
- [Poppins](https://fonts.google.com/specimen/Poppins)
- [Raleway](https://fonts.google.com/specimen/Raleway)
- [Operator](https://www.typography.com/fonts/operator/styles)

## Images

- [ICO](https://github.com/kevva/to-ico)
- [Images API](https://github.com/rsms/node-imagemagick)
- [JavaScript Load Image](https://github.com/blueimp/JavaScript-Load-Image)
- [Sharp](https://github.com/lovell/sharp)

### Image Color

- [Color Difference Library](https://github.com/lokesh/color-thief)

### Icons

- [Remix Icons](https://github.com/Remix-Design/remixicon)
- [Icon Font](https://www.iconfont.cn)
- [Icons8](https://icons8.com)
- [Ikonate](https://github.com/mikolajdobrucki/ikonate)
- [CSS Icons](https://cssicon.space)

### Emoji

- [OwO Keyboard Emoji](https://github.com/DIYgod/OwO)
- [Twitter Emoji](https://github.com/twitter/twemoji)
- [Emoji Panel](https://github.com/TimeToKnow/emoji-panel)

### SVG

- [React SVG Components](https://github.com/miukimiu/react-kawaii)
- [SVG.js](https://github.com/svgdotjs/svg.js)
- [SVG Optimizer](https://github.com/svg/svgo)
- [SVG Gallery](https://gallery.manypixels.co)
- [SVG Logos](https://github.com/gilbarbara/logos)
- [SVG Icons](https://iconsvg.xyz)
- [DVI2SVG](https://github.com/mgieseki/dvisvgm)

### Image Size

- [Variant Size Pictures](https://github.com/imulus/retinajs)

### Slide Images

- [placeholder.js](https://github.com/hustcc/placeholder.js)
- [Pictures Viewer Gallery](https://github.com/fengyuanchen/viewerjs)

### Image Gallery

- [Light Gallery](https://github.com/sachinchoolur/lightgallery.js)
- [Photo Swipe](https://github.com/dimsemenov/PhotoSwipe)

### Image Filter

- [Pictures Color Style Filter](https://github.com/we-are-next/cssco)
- [Rainy Day Effect](https://github.com/maroslaw/rainyday.js)
- [Image Difference Library](https://github.com/HumbleSoftware/js-imagediff)

## Canvas

- [HTML2Canvas](https://github.com/niklasvh/html2canvas)
- [Rough.js](https://github.com/pshihn/rough)
- [Canvas Manipulation](https://github.com/meltingice/CamanJS)

### Particles

- [HTML5 Particles](https://github.com/MapleRecall/html5-particles)
- [React Particle Animation](https://github.com/transitive-bullshit/react-particle-animation)
- [React Particle Button](https://github.com/transitive-bullshit/react-particle-effect-button)

### Blocks

- [Obelisk.js](https://github.com/nosir/obelisk.js)

### 3D Engine

- [CSS 3D Engine](https://github.com/shrekshrek/css3d-engine)
- [Three.js](https://github.com/mrdoob/three.js)
- [Krpano](https://krpano.com/docu/js/#top)

## Media

### Audio

- [Howler.js](https://github.com/goldfire/howler.js)
- [Music Helper Utils](https://github.com/madewithlove/music-fns)
- [Elementary Audio Tools](https://github.com/nick-thompson/elementary)
- [MIDI.js](https://github.com/mudcube/MIDI.js)

### Video

- [React Player](https://github.com/zhihu/griffith)
- [Video.js](https://github.com/videojs/video.js)
- [Plyr](https://github.com/selz/plyr)
- [FLV.js](https://github.com/bilibili/flv.js)

## Clipboard

- [Clipboard](https://github.com/zenorocha/clipboard.js)

## Keyboard

- [Hot Key](https://github.com/github/hotkey)

## Editor

### Rich Text Editor

- [React Markdown](https://github.com/rexxars/react-markdown)
- [Block Editor](https://github.com/codex-team/editor.js)
- [CKEditor](https://github.com/ckeditor/ckeditor5)
- [Wang Editor](https://github.com/wangfupeng1988/wangEditor)
- [Markdown Editor](https://github.com/RIP21/react-simplemde-editor)

### Code Editor

- [React Draft.js Editor](https://github.com/facebook/draft-js)
- [React ACE](https://github.com/securingsincity/react-ace)
- [ACE Editor](https://github.com/ajaxorg/ace)
- [Code Mirror](https://github.com/codemirror/CodeMirror)
- [Block Editor](https://github.com/codex-team/editor.js)

## SMS

### Phone

- [Twilio](https://github.com/twilio/twilio-node)

### Email

- [Node Emailer](https://github.com/nodemailer/nodemailer)
- [Email Parser](https://github.com/nodemailer/mailparser)
- [Email Generator](https://github.com/eladnava/mailgen)
- [MJML Markup Language](https://github.com/mjmlio/mjml)
- [IMAP](https://github.com/mscdex/node-imap)
- [MailSpring](https://github.com/Foundry376/Mailspring)

## File

- [zTree v3](https://github.com/zTree/zTree_v3)
- [FileAPI](https://github.com/mailru/FileAPI)

### File Uploader

- [React Filepond](https://github.com/pqina/react-filepond)
- [Vue Filepond](https://github.com/pqina/vue-filepond)
- [Uppy Uploader](https://github.com/transloadit/uppy)

### File Downloader

- [You Get](https://github.com/soimort/you-get)
- [Motrix](https://github.com/agalwood/Motrix)

### File Utils

- [Human Readable File Size](https://github.com/avoidwork/filesize.js)
- [Globby](https://github.com/sindresorhus/globby)
- [File Type](https://github.com/sindresorhus/file-type)

### PDF

- [PDFMake](https://github.com/bpampuch/pdfmake)
- [PDFKit](https://github.com/foliojs/pdfkit)

## Persistent Storage

- [PouchDB](https://github.com/pouchdb/pouchdb)
- [ImmortalDB](https://github.com/gruns/ImmortalDB)
- [lowdb](https://github.com/typicode/lowdb)
- [brownies](https://github.com/franciscop/brownies)
- [store.js](https://github.com/marcuswestin/store.js)
- [localForage](https://github.com/localForage/localForage)

## Search

- [React Search Bar](https://github.com/searchkit/searchkit)
- [SearchKit](https://github.com/searchkit/searchkit)
- [Full Text Search Engine](https://github.com/olivernn/lunr.js)

## CLI

### CLI Compiler

- [PKG](https://github.com/zeit/pkg)
- [NCC](https://github.com/zeit/ncc)

### CLI Library

- [Oclif: Open CLI Framework](https://github.com/oclif/oclif)
- [INK: React CLI App](https://github.com/vadimdemedes/ink)
- [Nexe: Node EXE Wrapper](https://github.com/nexe/nexe)
- [ZX: Ndoe Bash Wrapper](https://github.com/google/zx)
- [Commander](https://github.com/tj/commander.js)
- [Inquirer](https://github.com/SBoudrias/Inquirer.js)
- [Chalk](https://github.com/chalk/chalk)
- [ORA Spinner](https://github.com/sindresorhus/ora)
- [Progress](https://github.com/bvaughn/progress-estimator)
- [Babun: Windows Zsh](https://github.com/babun/babun)

### Terminal

- [React Terminal](https://github.com/rohanchandra/react-terminal-component)
- [React Console Emulator](https://github.com/js-rcon/react-console-emulator)
- [Jay: Supercharged JavaScript REPL](https://github.com/nikersify/jay)

## Daemon

- [PM2](https://github.com/Unitech/pm2)
- [Nodemon](https://github.com/remy/nodemon)

## Network

### Network Protocols

- [TelNet](https://github.com/mkozjak/node-telnet-client)
- [IMAP](https://github.com/mscdex/node-imap)

### Web Socket

- [Socket.IO](https://github.com/socketio/socket.io)

### P2P

- [FireFox Send](https://github.com/mozilla/send)

### Pre-Fetch

- [Google QuickLink](https://github.com/GoogleChromeLabs/quicklink)

### Lazy Loading

- [System.js](https://github.com/systemjs/systemjs)
- [Lazyload.js](https://github.com/rgrove/lazyload)
- [LAB.js: Await/Async Lazy Loading](https://github.com/getify/LABjs)

### Network Benchmark

- [HTTP/HTTPS Troubleshooting and Profiling](https://github.com/trimstray/htrace.sh)
- [HTTP/HTTPS Benchmarking Tool](https://github.com/mcollina/autocannon)

### Network Debugging

- [Whistle](https://github.com/avwo/whistle)

## Server

- [Parse Server](https://github.com/ParsePlatform/parse-server)

### Serverless

- [Serverless Framework](https://github.com/serverless/serverless)

## Encryption

- [MD5](https://github.com/blueimp/JavaScript-MD5)
- [Base64](https://github.com/dankogai/js-base64)

## Debug Testing

- [NDB](https://github.com/GoogleChromeLabs/ndb)
- [React Testing Utilities](https://github.com/airbnb/enzyme)
- [React Component Hierarchy](https://github.com/team-gryff/react-monocle)
- [React a11y](https://github.com/reactjs/react-a11y)
- [Retoggle: Component Inspector](https://github.com/Raathigesh/retoggle)

### Unit Testing

- [Jest](https://github.com/facebook/jest)
- [Jest UI](https://github.com/Raathigesh/majestic)
- [Enzyme](https://github.com/enzymejs/enzyme)
- [React Testing Library](https://github.com/testing-library/react-testing-library)
- [Jasmine](https://github.com/jasmine/jasmine)
- [Mocha](https://github.com/mochajs/mocha)
- [Assert](https://github.com/power-assert-js/power-assert)
- [Testem](https://github.com/testem/testem)

### Feature Testing

- [Karma](https://github.com/karma-runner/karma)
- [Webkit API(Chrome)](https://github.com/ariya/phantomjs)
- [Gecko API(Firefox)](https://github.com/laurentj/slimerjs)
- [Selenium](https://github.com/SeleniumHQ/selenium)
- [Interactor.js](https://github.com/wwilsman/interactor.js)

### End to End Testing

- [Cypress](https://github.com/cypress-io/cypress)
- [NightWatch: End to End Testing Framework](https://github.com/nightwatchjs/nightwatch)
- [LightHouse](https://github.com/GoogleChrome/lighthouse)
- [WebPageTest](https://github.com/WPO-Foundation/webpagetest-github-action)
- [WebHint](https://github.com/webhintio/hint)

### Headless Web Tools

- [Cheerio: jQuery Server Tools](https://github.com/cheeriojs/cheerio)
- [Puppeteer: Headless Chrome Tools](https://github.com/puppeteer/puppeteer)

### Code Analysis Tools

- [Babel.js](https://github.com/babel/babel)
- [AST Explorer](https://astexplorer.net)
- [Codecrumbs](https://github.com/Bogdan-Lyashenko/codecrumbs)

### Code Coverage Tools

- [Istanbul Coverage](https://github.com/gotwarlost/istanbul)
- [Karma Coverage](https://github.com/karma-runner/karma-coverage)

### Code Quality Tools

- [HTML Head Checklist](https://github.com/joshbuchea/HEAD)
- [ESLint Node Security](https://github.com/nodesecurity/eslint-plugin-security)
- [CSS Stats Tools](https://github.com/cssstats/cssstats)
- [CSS Stats CLI](https://github.com/projectwallace/wallace-cli)

### Inspect Tools

- [NDB](https://github.com/GoogleChromeLabs/ndb)
- [Reactotron](https://github.com/infinitered/reactotron)

### Monitoring Tools

- [NetData](https://github.com/netdata/netdata)
- [Source Buster](https://github.com/alexfedoseev/sourcebuster-js)
- [Uptime Status](https://github.com/yb/uptime-status)

### Performance Tools

- [React Re-Rendering Alert](https://github.com/welldone-software/why-did-you-render)
- [Node Clinic](https://github.com/nearform/node-clinic)
- [Perf Tools](https://github.com/brendangregg/perf-tools)
- [FlameGraph](https://github.com/brendangregg/FlameGraph)

### Log Tools

- [Log4.js](https://github.com/nomiddlename/log4js-node)
- [Stacktrace.js](https://github.com/stacktracejs/stacktrace.js)
- [Stacktrace Visualization](https://github.com/joyent/node-stackvis)
- [Log Analyzer](https://github.com/allinurl/goaccess)
- [HTTP Loger](https://github.com/expressjs/morgan)

### Mock Tools

- [Public APIs](https://github.com/public-apis/public-apis)
- [Mockery Function](https://github.com/mfncooper/mockery)
- [Mock Service Worker][https://github.com/mswjs/msw]
- [Nock Server](https://github.com/nock/nock)
- [JSON Server](https://github.com/typicode/json-server)
- [Images Mock](http://source.unsplash.com/random)
- [Images Placeholder](https://placeholder.com)
- [Pokemon API](https://github.com/PokeAPI/pokeapi)

### Security Tools

- [Sqlmap](https://github.com/sqlmapproject/sqlmap)
- [Zaproxy](https://github.com/zaproxy/zaproxy)
- [Arachni](https://github.com/Arachni/arachni)
- [Naughty Input Strings](https://github.com/minimaxir/big-list-of-naughty-strings))
- [FatRat](https://github.com/Screetsec/TheFatRat)
- [Spoof](https://github.com/feross/spoof)

### UML Tools

- [Draw.io](https://github.com/jgraph/drawio)
- [PlantUML](https://github.com/plantuml/plantuml)

## DevOps

### Project Tools

- [Node Maintenance Tools](https://github.com/maxogden/maintenance-modules)

### CI Tools

- [ProBot](https://github.com/probot/probot)

## Documentation

- [Docusaurus](https://github.com/facebook/docusaurus)
- [Vuepress](https://github.com/vuejs/vuepress)
- [TypeDoc](https://github.com/TypeStrong/typedoc)
- [Docz](https://github.com/pedronauck/docz)
- [DUmi](https://github.com/umijs/dumi)
- [Documentation.js](https://github.com/documentationjs/documentation)
- [Wiki.js](https://github.com/Requarks/wiki)
