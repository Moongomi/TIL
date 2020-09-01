#Controller & View
Controller에서 데이터를 처리해서 View에 표시합니다.<br/>
Controller -> View 의 간단한 소스 코드는 다음과 같습니다.<br/><br/>

```java
package pomo;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class HomeDescipt {
	@GetMapping("/")
	public String home() {
		return "h";
	}
}
```
return "h"라고 되어 있는 부분은 View에서 h라는 이름의 html과 같은 파일을 찾아 사용자에게 응답합니다.
