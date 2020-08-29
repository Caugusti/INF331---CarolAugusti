# INF331 - Lab 04

## Tarefa 1

> ![Tarefa 01 - Parte 1 - Components](images/Tarefa01_1.png)
> ![Tarefa 01 - Parte 2 - Components](images/Tarefa01_2.png)

## Tarefa 2
 
> ![Tarefa 02 - Controller e View](images/Tarefa02.png)

## Tarefa 3
 
> ![Tarefa 03 - Controller e Model](images/Tarefa03.png)

## Tarefa 4

### Serviço 1

* **Título do serviço**: `Consulta Spotify`

* **Breve descrição**:
  > `Consulta de dois álbuns de pop quaisquer.`
  
* **URL completa da requisição**: `<https://api.spotify.com/v1/search?limit=2&offset=0&q=pop&type=album&market=US>`

* **Cabeçalho HTTP da chamada**:
~~~http
Request Method: GET
Status Code: 200  (from disk cache)
~~~

~~~http
Accept: */*
Authorization: Bearer BQBBh9oz9NNV2CC0ULjUiyWGs2e5zoct5xGHVlu7fuu-S_VWzsD1Sr-EboPm3OfXMz-wjE2Y6MyTbCrm6HfUEl1JVudQKg2XZC28_2QsCDNPlq18qAV8Z4Hch62ra4S7xHDP8hdIa-Cicj1YQsUJApsAUntFFugjgN56HZeuRmPVvv0uRPbMaudDspVm78h3kGiNOB976q-PsdMXlHEeTu3lghEC12cJfZWeUstYkQUa5pgSTml2lPauGqt1HaTv1Q
Referer: https://any-api.com/spotify_com/spotify_com/console/_search/GET
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
~~~

* **Cabeçalho HTTP da resposta**:

~~~http
access-control-allow-credentials: true
access-control-allow-headers: Accept, App-Platform, Authorization, Content-Type, Origin, Retry-After, Spotify-App-Version, X-Cloud-Trace-Context
access-control-allow-methods: GET, POST, OPTIONS, PUT, DELETE, PATCH
access-control-allow-origin: *
access-control-expose-headers: content-type,cache-control,x-robots-tag,access-control-allow-origin,access-control-allow-headers,access-control-allow-methods,access-control-allow-credentials,access-control-max-age,content-encoding,strict-transport-security,x-content-type-options,date,server,via,alt-svc,connection,transfer-encoding,x-final-url
access-control-max-age: 604800
cache-control: public, max-age=7200
cf-cache-status: DYNAMIC
cf-ray: 5ca1dec78e16f76c-GRU
cf-request-id: 04d90990b10000f76ccc3e9200000001
content-encoding: br
content-type: application/json; charset=utf-8
date: Fri, 28 Aug 2020 23:39:12 GMT
expect-ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
server: cloudflare
status: 200
via: HTTP/2 edgeproxy, 1.1 google
x-content-type-options: nosniff
x-final-url: https://api.spotify.com/v1/search?limit=2&offset=0&q=pop&type=album&market=US
x-request-url: https://api.spotify.com/v1/search?limit=2&offset=0&q=pop&type=album&market=US
x-robots-tag: noindex, nofollow
~~~

* **Conteúdo da resposta**:
~~~json
{
  "albums" : {
    "href" : "https://api.spotify.com/v1/search?query=pop&type=album&market=US&offset=0&limit=2",
    "items" : [ {
      "album_type" : "single",
      "artists" : [ {
        "external_urls" : {
          "spotify" : "https://open.spotify.com/artist/0QHgL1lAIqAw0HtD7YldmP"
        },
        "href" : "https://api.spotify.com/v1/artists/0QHgL1lAIqAw0HtD7YldmP",
        "id" : "0QHgL1lAIqAw0HtD7YldmP",
        "name" : "DJ Khaled",
        "type" : "artist",
        "uri" : "spotify:artist:0QHgL1lAIqAw0HtD7YldmP"
      }, {
        "external_urls" : {
          "spotify" : "https://open.spotify.com/artist/3TVXtAsR1Inumwj472S9r4"
        },
        "href" : "https://api.spotify.com/v1/artists/3TVXtAsR1Inumwj472S9r4",
        "id" : "3TVXtAsR1Inumwj472S9r4",
        "name" : "Drake",
        "type" : "artist",
        "uri" : "spotify:artist:3TVXtAsR1Inumwj472S9r4"
      } ],
      "external_urls" : {
        "spotify" : "https://open.spotify.com/album/5nNtpPsSUgb9Hlb3dF1gXa"
      },
      "href" : "https://api.spotify.com/v1/albums/5nNtpPsSUgb9Hlb3dF1gXa",
      "id" : "5nNtpPsSUgb9Hlb3dF1gXa",
      "images" : [ {
        "height" : 640,
        "url" : "https://i.scdn.co/image/ab67616d0000b273efaecb4b9cbae7c120d14617",
        "width" : 640
      }, {
        "height" : 300,
        "url" : "https://i.scdn.co/image/ab67616d00001e02efaecb4b9cbae7c120d14617",
        "width" : 300
      }, {
        "height" : 64,
        "url" : "https://i.scdn.co/image/ab67616d00004851efaecb4b9cbae7c120d14617",
        "width" : 64
      } ],
      "name" : "POPSTAR (feat. Drake)",
      "release_date" : "2020-07-17",
      "release_date_precision" : "day",
      "total_tracks" : 1,
      "type" : "album",
      "uri" : "spotify:album:5nNtpPsSUgb9Hlb3dF1gXa"
    }, {
      "album_type" : "album",
      "artists" : [ {
        "external_urls" : {
          "spotify" : "https://open.spotify.com/artist/0eDvMgVFoNV3TpwtrVCoTj"
        },
        "href" : "https://api.spotify.com/v1/artists/0eDvMgVFoNV3TpwtrVCoTj",
        "id" : "0eDvMgVFoNV3TpwtrVCoTj",
        "name" : "Pop Smoke",
        "type" : "artist",
        "uri" : "spotify:artist:0eDvMgVFoNV3TpwtrVCoTj"
      } ],
      "external_urls" : {
        "spotify" : "https://open.spotify.com/album/7e7t0MCrNDcJZsPwUKjmOc"
      },
      "href" : "https://api.spotify.com/v1/albums/7e7t0MCrNDcJZsPwUKjmOc",
      "id" : "7e7t0MCrNDcJZsPwUKjmOc",
      "images" : [ {
        "height" : 640,
        "url" : "https://i.scdn.co/image/ab67616d0000b27377ada0863603903f57b34369",
        "width" : 640
      }, {
        "height" : 300,
        "url" : "https://i.scdn.co/image/ab67616d00001e0277ada0863603903f57b34369",
        "width" : 300
      }, {
        "height" : 64,
        "url" : "https://i.scdn.co/image/ab67616d0000485177ada0863603903f57b34369",
        "width" : 64
      } ],
      "name" : "Shoot For The Stars Aim For The Moon",
      "release_date" : "2020-07-03",
      "release_date_precision" : "day",
      "total_tracks" : 19,
      "type" : "album",
      "uri" : "spotify:album:7e7t0MCrNDcJZsPwUKjmOc"
    } ],
    "limit" : 2,
    "next" : "https://api.spotify.com/v1/search?query=pop&type=album&market=US&offset=2&limit=2",
    "offset" : 0,
    "previous" : null,
    "total" : 10002
  }
}
~~~

* **Parâmetros**:
> ![Tarefa 04 - Serviço 1](images/Tarefa04_Servico1.png)

### Serviço 2

* **Título do serviço**: `Consulta Open Skills`

* **Breve descrição**:
  > `Consulta de empregos que iniciam com a palavra "Software" e terminem com a palavra "Engineer".`
  
* **URL completa da requisição**: `<http://api.dataatwork.org/v1/jobs/autocomplete?begins_with=Software&ends_with=Engineer>`

* **Cabeçalho HTTP da chamada**:
~~~http
Request Method: GET
Status Code: 200
~~~

~~~http
:authority: any-api.com:8443
:method: GET
:path: /http://api.dataatwork.org/v1/jobs/autocomplete?begins_with=Software&ends_with=Engineer
:scheme: https
accept: */*
accept-encoding: gzip, deflate, br
accept-language: pt-BR,pt;q=0.9,en-US;q=0.8,en;q=0.7
origin: https://any-api.com
referer: https://any-api.com/dataatwork_org/dataatwork_org/console/_jobs_autocomplete/GET
sec-fetch-dest: empty
sec-fetch-mode: cors
sec-fetch-site: same-site
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
~~~

* **Cabeçalho HTTP da resposta**:

~~~http
access-control-allow-headers: Content-Type,X-Amz-Date,Authorization,X-Api-Key,X-Amz-Security-Token
access-control-allow-methods: *
access-control-allow-origin: *
access-control-expose-headers: date,server,access-control-allow-headers,access-control-allow-methods,access-control-allow-origin,content-length,connection,content-type,x-final-url
cf-cache-status: DYNAMIC
cf-ray: 5ca273a6783bf760-GRU
cf-request-id: 04d9669c070000f7601a8fb200000001
content-encoding: br
content-type: application/json
date: Sat, 29 Aug 2020 01:20:49 GMT
expect-ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
server: cloudflare
set-cookie: __cfduid=d81ddfabf1d5bea151875f1f6e1aa4ac71598664049; expires=Mon, 28-Sep-20 01:20:49 GMT; path=/; domain=.any-api.com; HttpOnly; SameSite=Lax
status: 200
x-final-url: http://api.dataatwork.org/v1/jobs/autocomplete?begins_with=Software&ends_with=Engineer
x-request-url: http://api.dataatwork.org/v1/jobs/autocomplete?begins_with=Software&ends_with=Engineer
~~~

* **Conteúdo da resposta**:
~~~json
[
  {
    "uuid": "11a3fde03891cabf49f6df1656abb0f6",
    "suggestion": "Software Publisher",
    "normalized_job_title": "software publisher",
    "parent_uuid": "c0f39f867727068f920213c55ed05939"
  },
  {
    "uuid": "76bf7eeacd105e6d1f517efab5b66481",
    "suggestion": "Software Installer",
    "normalized_job_title": "software installer",
    "parent_uuid": "9c4fa3af527c538e345640a28f2d0586"
  },
  {
    "uuid": "d93b8ce431c15639af93eebcb49effa6",
    "suggestion": "Software Trainer",
    "normalized_job_title": "software trainer",
    "parent_uuid": "9c4fa3af527c538e345640a28f2d0586"
  },
  {
    "uuid": "6dc58920d16d7526b69f904981244dbc",
    "suggestion": "Software Quality Engineer",
    "normalized_job_title": "software quality engineer",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "1cc06bc4a1e198c6267c347df4d8c1b5",
    "suggestion": "Software Tester",
    "normalized_job_title": "software tester",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "3a014dd9b348406df2998f3b4903347b",
    "suggestion": "Software Project Manager",
    "normalized_job_title": "software project manager",
    "parent_uuid": "c9b22af74071153203bd588bd45340d9"
  },
  {
    "uuid": "7c1a76c4c31058476f255402242d9927",
    "suggestion": "Software Consultant",
    "normalized_job_title": "software consultant",
    "parent_uuid": "0148f61d4227497728ce33490843d056"
  },
  {
    "uuid": "a9f4d9936d1ceaebaf43c217c972a23e",
    "suggestion": "Software Programmer",
    "normalized_job_title": "software programmer",
    "parent_uuid": "0b0c94f09f8afa4086c2bf44bd1bbcc4"
  },
  {
    "uuid": "ba11b06c352c4159bbe797cd8091dbf6",
    "suggestion": "Software Applications Architect",
    "normalized_job_title": "software applications architect",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "741055ee3eeeb86918098192f8edb9f8",
    "suggestion": "Software Applications Designer",
    "normalized_job_title": "software applications designer",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "c359a0b3a20b32ef1e0dfae41d3f761a",
    "suggestion": "Software Applications Engineer",
    "normalized_job_title": "software applications engineer",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "ff689f71893af57f31fe865173ce1cad",
    "suggestion": "Software Applications Specialist",
    "normalized_job_title": "software applications specialist",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "5b9cc7edb999cb36a39afdb0a8a6012a",
    "suggestion": "Software Computer Specialist",
    "normalized_job_title": "software computer specialist",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "06d525d9ce8acca3918e4017399e11af",
    "suggestion": "Software Designer",
    "normalized_job_title": "software designer",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "f5aa9a890f9a082766d3f23b7526ab66",
    "suggestion": "Software Development Specialist",
    "normalized_job_title": "software development specialist",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "14fa6e8b6cca66be98596c896d5a95fc",
    "suggestion": "Software Engineering Supervisor",
    "normalized_job_title": "software engineering supervisor",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "ec7eb73f54af07b4d3e918ec098a1b76",
    "suggestion": "Software QA Tester",
    "normalized_job_title": "software qa tester",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "545f37da310031f12018875c83084de0",
    "suggestion": "Software Quality Assurance Specialist",
    "normalized_job_title": "software quality assurance specialist",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "2fcb93ff09b684571fd504e7109a8c4d",
    "suggestion": "Software Requirements Engineer",
    "normalized_job_title": "software requirements engineer",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "2070859bfd79b7a3ac760e0ec429c6e2",
    "suggestion": "Software Writer",
    "normalized_job_title": "software writer",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "127c5a2025992d6408bdddaaa7247a4f",
    "suggestion": "Software Engineering Systems Information Technology Specialist",
    "normalized_job_title": "software engineering systems information technology specialist",
    "parent_uuid": "ad7f545d458070129f3ced2d13467813"
  },
  {
    "uuid": "83a694bade8d2b8436c8cb976e037983",
    "suggestion": "Software Quality Assurance Engineer (SQA Engineer)",
    "normalized_job_title": "software quality assurance engineer sqa engineer",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "a0d34bd06b9d8f0f70788285333c21c3",
    "suggestion": "Software Quality Tester",
    "normalized_job_title": "software quality tester",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "acb6ea1fd5eedf9ea80cd704f159c913",
    "suggestion": "Software Test Analyst",
    "normalized_job_title": "software test analyst",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "f39b284c7db0a0fe55e205882f977364",
    "suggestion": "Software Test Engineer",
    "normalized_job_title": "software test engineer",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "c8d12f88d98175133a2b88be9223a466",
    "suggestion": "Software Testing Specialist",
    "normalized_job_title": "software testing specialist",
    "parent_uuid": "3743e28a587c5e3b2c5b3793333db9a5"
  },
  {
    "uuid": "15e32cbec22a211c482d2c20831dfaca",
    "suggestion": "Software Development Project Manager",
    "normalized_job_title": "software development project manager",
    "parent_uuid": "c9b22af74071153203bd588bd45340d9"
  },
  {
    "uuid": "f95410df55aa318834018cfc532fded4",
    "suggestion": "Software Technician",
    "normalized_job_title": "software technician",
    "parent_uuid": "16a750537ecaff343d0e1d9ab9f5f575"
  },
  {
    "uuid": "01af60dca22fed9bf9b7226dca87107f",
    "suggestion": "Software Analyst",
    "normalized_job_title": "software analyst",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "23a71ce4809b6115e337bb22797ae52f",
    "suggestion": "Software Design Engineer",
    "normalized_job_title": "software design engineer",
    "parent_uuid": "ad7f545d458070129f3ced2d13467813"
  },
  {
    "uuid": "f584b59fa698ebfda3a7b24f6e408dbe",
    "suggestion": "Software Systems Engineer",
    "normalized_job_title": "software systems engineer",
    "parent_uuid": "ad7f545d458070129f3ced2d13467813"
  },
  {
    "uuid": "cde69d2abb5f635ebc7f0379448992ef",
    "suggestion": "Software Development Engineer",
    "normalized_job_title": "software development engineer",
    "parent_uuid": "adbc2046a7264152d61d23ecdc1606b3"
  },
  {
    "uuid": "6b0b1cc3de799472d984e6346b929e51",
    "suggestion": "Software Architect",
    "normalized_job_title": "software architect",
    "parent_uuid": "ad7f545d458070129f3ced2d13467813"
  },
  {
    "uuid": "a8f342c21860ef255af3867e5a4a71b2",
    "suggestion": "Software Developer",
    "normalized_job_title": "software developer",
    "parent_uuid": "ad7f545d458070129f3ced2d13467813"
  },
  {
    "uuid": "4b7281a983a4574eb887d29f7fbebd88",
    "suggestion": "Software Engineer",
    "normalized_job_title": "software engineer",
    "parent_uuid": "6b6e7eda0f21fd2d8e1edf2394523743"
  }
]
~~~

* **Parâmetros**:
> ![Tarefa 04 - Serviço 2](images/Tarefa04_Servico2.png)
