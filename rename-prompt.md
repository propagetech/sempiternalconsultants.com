You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/6d95c421cfdc25743ca3bee482775041.css",
    "context": {
      "path": "css/6d95c421cfdc25743ca3bee482775041.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css",
    "context": {
      "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/085527357fd95c44b1a4513d3b084801.webp",
    "context": {
      "refs": [
        {
          "alt": "Office",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1da86d1c29f5ed9415ded9cb8da86af0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/2255d146270d61f71d4a8df42c5a98ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/253f643c194205893a565f31f2a09be8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/429d8ab5969ad703ab323320abe35734.webp",
    "context": {
      "refs": [
        {
          "alt": "Office",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4dd794fef5382d202d02d568cf169bfd.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ea921b05154824904fa5519cd0dff49.webp",
    "context": {
      "refs": [
        {
          "alt": "Office",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5fb14b0d12ae4b73f237f6df39ecbf91.webp",
    "context": {
      "refs": [
        {
          "alt": "healthcare",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65854b2f99e8b14f429dfa9c2b7619aa.webp",
    "context": {
      "refs": [
        {
          "alt": "001",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d7dae6f43613a301e5815874bfb3803.webp",
    "context": {
      "refs": [
        {
          "alt": "VALUES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7330fda946da17693e18b92b0b65ee66.webp",
    "context": {
      "refs": [
        {
          "alt": "Management Consultancy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7dac80e6668a704e16e106649d8f1c9e.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b615a41a178f6f42285617632dbb718.webp",
    "context": {
      "refs": [
        {
          "alt": "Aeroplane",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e79dccd1247c43f3048120fb51e172b.webp",
    "context": {
      "refs": [
        {
          "alt": "Aeroplane",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96f0988ac05f5d40c7e27715682ebc96.webp",
    "context": {
      "refs": [
        {
          "alt": "Business Structuring",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a8de3edb530160c6333f45ca4eed160.webp",
    "context": {
      "refs": [
        {
          "alt": "003",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ca75872dfb33d3cdaa5836afbd2fe5d.webp",
    "context": {
      "refs": [
        {
          "alt": "005",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9cdf7398bfea1f8bd729cb06b6275fd3.webp",
    "context": {
      "refs": [
        {
          "alt": "004",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1e8ca1e1e3cc94d913e8ee11d23343e.webp",
    "context": {
      "refs": [
        {
          "alt": "VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a826e2cc9688abf7d723bdb1482e7438.webp",
    "context": {
      "refs": [
        {
          "alt": "healthcare",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b822b35ae91c73a3b43726151671ef84.webp",
    "context": {
      "refs": [
        {
          "alt": "Financial Engineering",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9ba95e37383e930ea2940e895a488c5.webp",
    "context": {
      "refs": [
        {
          "alt": "002",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb45e609e837531cd706d2fd02b30a0d.webp",
    "context": {
      "refs": [
        {
          "alt": "Project Advisory Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd612d1034e01b86220fe1278a885577.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfb2a4c519f766793c525e1b0ec8856b.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9d5350bcdd1e74df2d53842ab385962.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebfa6977ec49a0060814a488b2fc706b.webp",
    "context": {
      "refs": [
        {
          "alt": "Aeroplane",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f730c33813f7550fc95f31c23a75f924.webp",
    "context": {
      "refs": [
        {
          "alt": "healthcare",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbd60676d9209e755efb4915210f46cd.webp",
    "context": {
      "refs": [
        {
          "alt": "006",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Sempiternal Consultants LLP | One Stop Innovative Solutions",
      "first_heading": "Sempiternal Consultants LLP"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.