### Using [wrk](https://github.com/wg/wrk) to benchmark various web frameworks and some of my personal blog site routes

```json
{
    "test params": {
        "args": "./wrk -t12 -c400 -d30s"
    },
    "testing hardware": {
        "cpu": "intel i9 9900k @4.8ghz",
        "ram": "32gb ddr4",
        "gpu": "nvidia 1080",
    },
    "vanilla builds | response type = text/plain | single route '/'": {
        "go/fiber": {
            "verions": {
                "go": "1.17",
                "fiber": "2.17"
            },
            "requests/sec": 959756.93
        },
        "nim/jester": {
            "verions": {
                "nim": "1.4.8",
                "jester": "0.5.0"
            },            
            "requests/sec": 922239.20
        },
        "rust/warp": {
            "verions": {
                "rust": "1.54.0",
                "warp": "0.3.1"
            },          
            "requests/sec": 779977.38
        },
        "go/echo": {
            "verions": {
                "go": "1.17",
                "echo": "4.5.0"
            },
            "requests/sec": 513006.20
        },
        "nim/prologue": {
            "verions": {
                "nim": "1.4.8",
                "prologue": "0.4.8"
            },          
            "requests/sec": 488949.83
        },
        "nodejs/uWebSockets.js": {
            "verions": {
                "node": "16.7.0",
                "uWebSockets.js": "19.3.0"
            },          
            "requests/sec": 200507.56
        },
        "nodejs/nanoexpress": {
            "verions": {
                "node": "16.7.0",
                "Nanoexpress": "5.0.8"
            },          
            "requests/sec": 123570.63
        },
        "nodejs/koa": {
            "verions": {
                "node": "16.7.0",
                "Koa": "2.13.1"
            },          
            "requests/sec": 32818.44
        }
    },
    "blog.wildwooddev.com route: /blog": {
        "nim/jester": {
            "date": "august 25, 2021",
            "commit": "b2447334cda69add7c699739f0485d3a6e3a9488", 
            "verions": {
                "nim": "1.4.8",
                "jester": "0.5.0"
            },      
            "requests/sec": 20507.45,
            "comments": "rewrote date sort proc with custom date string comparsion, 4x the performance"
        },
        "go/fiber": {
            "verions": {
                "go": "1.17",
                "Fiber": "2.17"
            },
            "requests/sec": 5447.74
        },
        "nim/jester": {
            "verions": {
                "nim": "1.4.8",
                "jester": "0.5.0"
            },      
            "requests/sec": 4752.14
        },
        "nim/prologue": {
            "verions": {
                "nim": "1.4.8",
                "prologue": "0.4.8"
            },   
            "requests/sec": 4746.31
        },
        "nodejs/koa": {
            "verions": {
                "node": "16.7.0",
                "Koa": "2.13.1"
            },   
            "requests/sec": 592.85
        }
    }
}
```