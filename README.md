### Using `wrk` to benchmark my blog website builds and also bench vanilla builds for fun!

```json
{
    "Test Params": {
        "args": "./wrk -t12 -c400 -d30s"
    },
    "vanilla builds | response type = text/plain": {
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
        "go/fiber": {
            "verions": {
                "go": "1.16",
                "Fiber": "2.16"
            },
            "requests/sec": 5457.74
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