# HTTP/2 in Action 문제 모음

## 1장 웹 기술과 HTTP

1. 브라우저에 `www.google.com`이동한다고 가정해 봅시다. 우리가 웹페이지를 볼때까지 어떤 과정을 거쳐서 보이게 되는지 설명해 주세요
2. HTTP가 무엇이고 HTTP/1.1까지 어떻게 진화했는지 설명해 주세요
3. HTTP헤더의 이름은 대소문자를 구분하나요?
4. HTTP헤더를 명시하는 방법에 대해서 설명해 주세요.
5. HTTP/0.9에서는 줄 바꿈 문자를 하나만 사용해도 되는데 HTTP/1.0부터는 줄바꿈 문자를 2개 써야 합니다. 그 이유에 대해서 설명해 주세요.
6. 동일한 형식의 헤더를 여러개 보내면 어떻게 되나요?
7. HTTP 응답코드는 2xx(성공), 3xx(리다렉션), 4xx(클라이언트 오류), 5xx(서버 오류)로 분류되어 있습니다. 이렇게 분류되어 있는 이유는 무엇인가요?
8. HTTP/1.1에서 Host 헤더가 필수적으로 포함된 이유는 무엇인가요? 필수로 포함되어 생긴 문제는 무엇인가요?
9. Connection: Keep-Alive가 생긴 이유는 무엇인가요?
10. HTTPS란 무엇이고 어떤 문제 때문에 나오게 되었나요?
11. HTTPS는 HTTP 메시지에 암호화, 무결성, 인증을 추가했습니다. 각각에 대해 설명해 주세요.
12. HTTPS의 키를 교환할 때 공개키 암호화를 통해서 교환하는 이유는 무엇일까요?
13. HTTPS가 동작하는 과정에 대해서 설명해 주세요.
14. 기본적인 HTTP 도구들에는 무엇이 있나요?

## 2장 HTTP/2를 향한 여정

1. HTTP/1.1의 근본적인 성능 문제란 무엇인가요?
2. HTTP/1.1에서 파이프라이닝이 잘 쓰이지 않은 이유는 무엇인가요?
3. HTTP/1.1의 성능 문제를 우회해서 해결하는 방법에는 2가지가 있습니다. 1. 여러 HTTP 연결을 사용한다. 2. 적지만 잠재적으로 큰 HTTP 요청을 만든다. 각 해결책에 대해서 설명하고 한계점에 대해서도 설명해 주세요.
4. HTTP/1.1에서 브라우저가 도메인 당 요청 수를 6개로 제한한 이유는 무엇인가요?
5. HTTP/1.1은 텍스트 기반 프로토콜입니다. 그래서 요청과 헤더도 텍스트 기반인데요. 이로인해 생기는 문제는 무엇인가요?
6. HTTP-NG는 실패하고 SPDY는 성공할 수 있었던 이유는 무엇인가요? 
7. SPDY가 HTTP/1을 어떻게 개선했나요?
8. SPDY가 HTTP/2로 표준화된 과정은 무엇인가요?
9. 만약 HTTP/2를 적용했는데 성능에 큰 이점이 없었다. 무엇을 의심해봐야 할까?
10. HTTP/1.1의 성능 문제를 우회하는 방법이 HTTP/2에서 안티패턴이 되는 이유는 무엇인가요?

## 3장 HTTP/2로 업그레이드

1. 내가 서비스 중인 앱에 새로운 웹 기술을 사용하려고 합니다. 무엇을 고려해서 기술을 도입해야 할까요?
2. HTTP/2의 사양은 HTTPS에서만 동작한다는 사양은 존재하지 않는다. 하지만 대부분의 브라우저는 HTTPS를 강제하고 있는데 그 이유에 대해서 설명해 주세요.
3. 서버에 HTTP/2를 활성화 하는데 있어서 어려움은 어떤 것이 있을까요?
4. 어떤 이유로 인해 애플리케이션 서버를 HTTP/2를 활성화가 불가능하다고 가정해 봅시다. 이럴 때 HTTP/2를 활성화 하기 위해서 어떤 대안이 있나요?
5. 리버스 프록시와 애플리케이션 서버와의 통신은 HTTP/1.1로 해도 성능문제가 그렇게 심하지 않은데, 그 이유는 무엇일까요?
6. HTTP/2를 활성화를 하고 테스트 해봤더니, HTTP/2가 올바르게 동작하지 않습니다. 이럴 때 무엇을 의심해 볼 수 있을까요?

## 4장 HTTP/2 프로토콜 기초

1. HTTP/2에서 새롭게 추가된 개념 여섯가지에 대해 설명해 주세요.
2. HTTP에서 HTTPS를 도입할 때는 웹 사이트를 개발하는 방식에는 영향을 주지 않는다. 하지만 HTTP/2는 웹 사이트를 개발하는 방식을 다르게 가져가야 하는데 그 이유는 무엇인가?
3. HTTP/2가 단일 연결에서 어떻게 동시에 여러 개의 요청이 어떻게 가능한지 작동 방식을 설명해 주세요.
4. 스트림 우선순위화가 필요한 이유에 대해서 설명해 주세요
5. HTTP/1.1은 TCP 흐름 제어에 의존하여 전송 속도를 조절할 수 있습니다. 반면에 HTTP/2가 TCP 흐름 제어에 의존할 수 없는데, 그 이유를 설명해 주세요.
6. HTTP/2는 HTTPS처럼 새로운 포트를 사용하거나 프로토콜(`https://`)을 변경하지 않기로 했습니다. 그대신에 클라이언트와 서버가 HTTP/1.1 대신 HTTP/2로 연결하는 방법에 대해서 설명해 주세요.
7. HTTPS의 핸드 쉐이크 과정에 대해서 설명해 주세요
8. HTTP/2 프레임에 대해서 설명해 주세요.

## 5장 HTTP/2 푸시의 구현

1. 라운트 트립 지연이란 무엇일까요?
2. 라운드 트립 지연을 해결하기 위한 방법으로 중요 리소스를 인라이닝 할 수 있습니다. 이 인라이닝에 대해서 설명하고 한계점에 대해서도 설명해 주세요.
3. 라운드 트립 지연 문제를 HTTP/2 푸시가 어떻게 해결할 수 있나요?
4. HTTP/2 푸시 방식은 1. HTTP Link 헤더를 사용하여 웹서버가 푸시 2. 애플리케이션에서 직접 푸시 방식이 있습니다.
    1. HTTP Link헤더를 사용해 웹 서버가 푸시를 하도록 할 경우 1. 웹 서버에 직접 설정 2. 링크 헤더를 사용 3. 103 Early Hints 사용 할 수 있습니다. 각 방법에 대해서 설명해 주세요.
    2. HTTP/2 푸시를 애플리케이션 서버에서 직접 구현하는 것의 단점은 무엇인지 설명해 주세요.
5. 브라우저에서 HTTP/2 푸시로 받은 리소스를 어떻게 사용하는지 그 과정을 설명해 주세요.
6. 이미 브라우저가 리소스를 가지고 있는데, 서버에서 또 리소스를 푸시하는 것은 낭비입니다. 
    1. RST_STEAM 프레임을 사용해서 리소스를 거절, 서버측에 클라이언트에 푸시된 리소스를 기록, 클라이언트가 푸시된 리소스를 기록, if-modifield-since헤더나 etag헤더를 통해 판단, 캐시 다이제스트를 사용하는 방법들이 있습니다. 각 방법에 대해서 설명하고 한계점에 대해서도 설명해 주세요.
7. HTTP/2 푸시는 규칙때문에 GET 요청만 푸시된다. 그 이유에 대해서 설명해 주세요.
8. 모든 리소스를 푸시하면 안되는 이유에 대해서 설명해 주세요.
9. HTTP/2 푸시가 올바르게 동작하는지 확인하려고 봤더니 푸시된 리소스가 없다. 어떤 문제가 의심되고 어떻게 해결해야 하는지 설명해 주세요.
10. 성능 개선을 위해 푸시를 사용하지만 느리게 만드는 위험성도 존재한다. 그 대안으로 프리로드를 사용할 수 있는데, 프리로드가 가진 장점에 대해서 설명해 주세요.

## 6장 HTTP/2 최적화

1. 만약 HTTP/2를 도입하기로 결정되었다면, 자신의 개발하는 과정에 있어서 어떤
   영향이 있을지 설명해 주세요.
2. HTTP/2는 HTTP/1.1에서 필요했던 만큼 번들링이 필요할까요? 어떻게 판단해야
   할까요?
3. HTTP/2에서도 샤딩이 필요할까요?
4. HTTP/2에서도 인라이닝이 필요할까요?
5. HTTP/2는 HTTP/1.1의 성능 문제를 해결합니다. 하지만 한계점도 존재하는데요. 이
   한계점에 대해서 설명해 주세요.
6. HTTP/1.1과 HTTP/2를 어떻게 최적화해야 하는지 설명해 주세요.
7. HTTP/2 연결을 여러 도메인에 재사용할 수 있는 조건은 무엇인가요?
8. HTTP 상태 코드 421이 새로 도입된 배경은 무엇인가요?

## 7장 고급 HTTP/2 개념

1. HTTP/2 스트림과 HTTP/1.1 연결을 비교해서 설명해 주세요
2. HTTP/2 스트림을 종료하거나 여는 비용은 HTTP/1.1 연결을 여는 데 드는 비용 보다 상당히 적습니다. 그 이유를 설명해 주세요.
3. HTTP/2 스트림의 수명주기에 대해서 설명해 주세요.
4. TCP에서 이미 흐름 제어가 있는데, HTTP/2에서 따로 흐름 제어가 필요한 이유에 대해서 설명해 주세요.
5. HTTP/2 흐름 제어가 어떻게 동작하는지 설명해 주세요.
6. 스트림 흐름 제어 window는 HTTP/2 연결마다 하나씩 있다 vs 각 스트림 마다 흐름 제어 window가 존재한다.
7. HTTP/2 우선순위는 두 가지 방식으로 정의됩니다. 이 방식은 무엇인가요?
8. 만약 second.js가 main.js에 의존하고 있다고 가정해 보겠습니다. 만약 main.js를 처리하느라 보낼 수 없는 경우 second.js는 main.js가 준비될때까지 기다릴까요?

## 8장 HPACK 헤더

1. 헤더 압축이 필요해진 이유는 무엇일까요?
2. 무손실 압축과 손실 압축의 차에 대해서 설명해 주세요. 그리고 헤더 압축은 어떤 압축을  사용해야 하는지 설명해 주세요.
3. 조회 테이블 압축 방법, 더 효율적인 인코딩 기법, 룩백 압축 방법에 대해서 설명해 주세요. 그리고 압축 방법들을 비교해서 언제 어떤 것을 사용해야 하는지 설명해 주세요.
4. 헤더를 통해서 브라우저와 서버가 압축 방법을 결정할 수 있습니다. 이 과정에 대해서 설명하고 왜 이렇게 만들어졌는지도 설명해 주세요.
5. Deflate 기반 압축은 보안 문제가 있다는 것이 밝혀졌습니다. Deflate의 어떤 속성 때문에 이러한 문제가 발생했나요?
6. HTTP/2가 자체적인 HTTP 헤더 압축 기법을 필요로 하는 이유는 무엇인가요?
7. HAPCK으로 헤더를 압축하는 방법을 설명해 주세요.
8. HPACK으로 압축된 헤더를 해제하는 방법을 설명해 주세요.

## 9장 TCP, QUIC, HTTP/3

1. TCP는 어떻게 무결성을 보장하나요?
2. TCP의 비효율성은 무엇이고 HTTP/2에 어떤 영향을 미치나요?
3. 혼잡 제어란 무엇인가요?
4. TCP의 혼잡 제어는 왜 비효율적인가요?
5. TCP의 느린 시작이 HTTP 프로토콜에 미치는 영향은 무엇인가요?
6. 패킷 손실 상황에는 HTTP/2가 오히려 HTTP/1.1보다 더 느릴 수 있습니다. 그 이유를 설명해 주세요.
7. HTTP/2에서 스트림을 전송하는 중에 패킷 손실이 일어난다면 어떤 일이 일어나는지 설명해 주세요.
8. TCP를 최적화하는 방법에는 무엇이 있나요?
9. QUIC은 HTTP/2의 어떤  문제를 해결하려고 하나요?
10. 왜 QUIC은 TCP를 개선하지 않고 UDP위에서 구현했나요?

## 10장 HTTP가 나아가는 방향

1. HTTP/2가 해결하지 못한 문제에 대해서 설명해 주세요.
2. 쿠키란 무엇이고 어떤 문제가 있는지 설명해 주세요.
3. 앞으로 새로운 HTTP 메서드가 추가될까요?
4. 앞으로 새로운 HTTP 헤더는 더 많이 추가될까요?
5. 초기의 HTTP는 웹 페이지를 불려오려고 만들어졌지만, 지금은 다양한 방법으로 사용될 수 있습니다. 그 방법들에 대해서 설명해 주세요.

## 출처

- [제 32회 코드숨 스터디](https://www.codesoom.com/courses/soomtudy?utm_source=%08github&utm_medium=repo&utm_campaign=http2-in-action)
- [HTTP/2 in Action \| 배리 폴라드 저자(글) · 임혜연 번역 \| 에이콘출판](https://product.kyobobook.co.kr/detail/S000001804952)

