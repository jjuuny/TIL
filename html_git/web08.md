# TIL Day08

## 0714

### googleMap

1. Google맵 라이브러리 연결

`<script async defer src="https://maps.googleapis.com/maps/api/js?key=키 값&callback=initMap">	</script>`

2. 위도, 경도를 이용한 객체를 생성해줘야 한다.    (위도와  경도 변수를 지정했다고 가정.)

`var myCenter = new google.maps.LatLng(latitude, longitude);`

3. 표시할 지도 옵션

```html
		  var mapProperty = {
			center : myCenter,
			zoom : 14, // 확대 : 0~21사이 값 숫자가 클수록 확대된다.
			mapTypeId : google.maps.MapTypeId.ROADMAP // 지도 종류(ROADMAP, HYBRID, 			STEELITE, TERRAIN)
			};
			var map = new google.maps.Map(document.getElementById("googleMapView"), 			mapProperty); // (지도를 표시할 곳, 맵옵션)
			
```

4. 마커표시하기

5. 정보 대화상자
6. 이벤트 등록
7. 반경 표시



jquery/jq01부터 jq04까지

**개발이 완료된 걸 배포하는 법**

1. 이클립스에서 프로젝트 만들고 war로 압축한다.
2. 파일을 서버(war)에 webapps에 복사한다
3. 서버 start하면 압추이 알아서 풀린다.