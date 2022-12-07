# qianduan-daima
1.1 监听网页是否调用某个接口
```js
const observer = new PerformanceObserver(_ => {
		if (performance.getEntriesByName("接口ip")
			.length >
			0) {
			console.log('网页调用该接口')
		}

	});
	observer.observe({
		entryTypes: ["resource"]
	})
