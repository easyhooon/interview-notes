# Android 면접 준비

정리일: 2026-10-11. 개인 면접 준비 노트.

## 사용 기준

- 아래 30초 답변은 본인의 설명으로 확인한 입장과 기존 Android 문서에 근거한 말하기 초안이다. 실제 발화 속도에 맞춰 줄인다.
- 회사 코드·로그와 측정 원문을 독립 확인하지 못한 부분은 기존 문서 진술로 구분한다. 지원 당시 제출 파일·제출일은 식별되지 않았다.
- 기존 Android 근거: [이력서](https://github.com/easyhooon/resume/blob/main/RESUME.md), [포트폴리오](https://github.com/easyhooon/resume/blob/main/PORTFOLIO.md), [경력기술서](https://github.com/easyhooon/resume/blob/main/CV.md).
- 확인되지 않은 성과 수치·회사 전체 구조·인증 동기화 해결 완료·약관 대응 완료를 만들지 않는다.
- Q9는 이미 준비하고 블로그도 작성한 사례여서 추가 반복 연습 우선순위가 낮다. Q10은 수치의 측정 조건과 싱글플라이트 적용 근거 확인이 우선이다.

## Q1. 우리 회사에 지원한 이유는 무엇인가요?

### 30초 답변

여비라는 여행 경비 앱을 만들면서 여행에서 생기는 불편을 제품으로 해결하는 데 관심이 생겼습니다. 지원 회사 Android 개발자와 인턴의 기술 블로그에서 경험을 공유하는 모습을 보며, 저도 블로그와 오픈소스로 배운 것을 공유해온 점에서 공감했습니다. 앱 출시·운영과 오류 대응 경험으로 사용자 흐름을 개선하고, 동료들과 설계와 코드를 논의하며 더 나은 선택을 하는 데 기여하고 싶습니다.

### 꼬리질문

- 여비에서 해결한 여행 불편과 본인 역할은 무엇이었나요?
- 실제 읽은 회사 기술 블로그 글에서 인상 깊었던 기술적 판단은 무엇인가요?
- 지원 회사 서비스의 사용자 흐름 중 본인 경험을 연결할 부분은 무엇인가요?

### 근거·미확인

여비 경험·공유 문화에 대한 동기는 본인 설명. 기존 포트폴리오의 YeoBee 및 블로그·OSS 활동과 연결한다. 실제 읽은 글 제목과 내용은 아직 확인되지 않았다. 추천 자료는 회사 기술 블로그의 WebView 토큰 관련 글이며, 실제 읽었다고 말하지 않는다. 현재 앱 전체 WebView 비율도 미확인이다.

## Q2. 이직하려는 이유는 무엇인가요?

### 30초 답변

현재 회사에서는 WebView와 네이티브 연동, BLE 건강 데이터, 카메라와 운영 문제를 다루며 경험을 쌓았습니다. 최근에는 프론트엔드와 자동화로 역할도 넓혔습니다. 이 경험을 바탕으로 Android 핵심 기능의 성능과 사용자 경험을 더 깊게 개선하고, 동료 개발자와 설계·코드 리뷰를 통해 선택을 검증하는 기회를 넓히고 싶어 지원했습니다.

### 꼬리질문

- 지금 회사에서 얻은 가장 큰 경험은 무엇인가요?
- Android에서 더 깊게 다루고 싶은 사용자 문제는 무엇인가요?
- Product Engineer 관심과 Android 지원은 어떻게 연결되나요?

### 근거·미확인

회사 비난이나 프론트엔드·PE 관심 포기를 전제로 하지 않는다. 지원 회사 내부 리뷰 방식은 직접 확인되지 않았으므로 실제 문화에 대한 단정 대신 희망과 기여 의지를 말한다.

## Q3. WebView 중심 경험을 Android 개발에 어떻게 활용할 수 있나요?

### 30초 답변

WebView를 다뤘지만 실제로 해결한 문제는 기기와 OS의 생명주기, 카메라·BLE 연동, 백그라운드 미디어와 상태 복구였습니다. 특히 앱 프로세스와 Renderer 종료를 구분하고 로그를 보강해 원인을 좁힌 경험은 네이티브 운영 문제에도 적용할 수 있습니다. Compose는 사이드 프로젝트 출시와 이번 과제에서 사용해왔고, 기존 운영 경험과 함께 Android 사용자 흐름을 안정화하는 데 활용하고 싶습니다.

### 꼬리질문

- 웹과 네이티브 책임을 어떤 기준으로 나눴나요?
- 백그라운드 진입·복귀 시 재생 위치와 상태는 어떻게 맞췄나요?
- 기기별 문제를 재현하기 어려울 때 어떤 로그를 추가했나요?

### 근거·미확인

PORTFOLIO의 Hi-me 트러블슈팅, RESUME의 BLE·MediaSession·Compose 경험. WebView 인증 동기화는 간헐 문제 제기만 있었으며 해결 완료 성과로 사용하지 않는다. 미디어 요청의 인증 헤더 갱신 경험과 WebView 인증 동기화는 별개다.

## Q4. 과제에서 가장 우선한 것은 무엇인가요?

### 30초 답변

오류가 나거나 화면을 이동해도 사용자가 진행하던 흐름을 이어갈 수 있게 하는 데 우선순위를 뒀습니다. 즐겨찾기는 Room에 저장하고, 검색 조건과 목록 스크롤 상태는 각각의 수명에 맞춰 분리했습니다. 정상 동작만 보는 대신 화면 이동과 취소 상황도 확인했고, 자동화한 실기기 검증으로 주요 사용자 흐름을 점검했습니다.

### 꼬리질문 — 복원

- 구성 변경·화면 복귀·프로세스 종료를 각각 어떻게 다뤘나요?
- 저장된 즐겨찾기와 진행 중인 쓰기의 보장은 어떻게 다른가요?
- 검색 조건과 스크롤을 같은 객체에 넣지 않은 이유는 무엇인가요?

### 근거·미확인

과제 구현·검증에 대한 본인 설명. Room에 이미 완료된 저장은 유지하지만 프로세스 종료 중 미완료 쓰기까지 완료된다고 보장하지 않는다. 실기기 검증의 정확한 목록·반복 횟수는 해당 QA 기록을 확인한 뒤 답한다.

## Q5. ViewModel 대신 retain을 사용한 이유는 무엇인가요?

### 30초 답변

Compose에서 일반 상태 객체를 ViewModel 상속 없이 유지하는 방식을 적용해보고 싶었습니다. DroidKaigi 사례를 참고해 Android 범위에서 적용했고, 객체를 유지하는 것과 프로세스 종료 후 저장된 값으로 복원하는 것은 분리했습니다. 대신 ViewModel이 제공하는 수명·코루틴 지원을 직접 책임져야 하므로, 화면 이동과 구성 변경에서 생성·정리가 의도대로 되는지 검증했습니다. ViewModel보다 항상 낫다는 선택은 아닙니다.

### 꼬리질문 — 수명·Scope

- retain이 프로세스 종료를 견디나요? → 아니다. 객체 유지와 직렬화된 상태 복원은 별개다.
- ViewModel의 장점은 무엇인가요? → ViewModelStore 범위, coroutine/DI/SavedState 통합 등 기본 지원을 갖는다.
- Activity나 View를 retain하면 어떤 위험이 있나요? → 더 짧은 수명의 객체 참조로 누수 가능성이 생긴다.
- 직접 관리한 Scope는 어디에서 종료하나요? → 과제의 실제 소유자와 정리 경로를 코드로 설명한다.

### 근거·미확인

공식 [State lifespans](https://developer.android.com/develop/ui/compose/state-lifespans), [ViewModel overview](https://developer.android.com/topic/libraries/architecture/viewmodel). 공식 문서도 두 방식의 수명·기능 차이를 구분한다. 공식적으로 ViewModel 대체를 일반 권장한다고 표현하지 않는다.

## Q6. Soil을 선택한 이유와 실제로 활용한 장점은 무엇인가요?

### 30~45초 답변

프론트엔드를 병행하며 TanStack Query의 서버 상태 관리 방식에 관심이 생겼습니다. 특히 API 호출 전후의 isLoading/finally/isError와 캐시 관리 코드를 화면마다 반복하는 점이 번거로웠습니다. 과제에서는 데이터 계층의 SearchBooksQueryKey가 Retrofit 요청·변환·요청 정책을 정의하고, Soil InfiniteQuery가 실행·캐시·로딩·오류 상태를 관리합니다. Presenter는 그 상태를 화면용 불변 UiState로 변환합니다. 별도 중계용 Repository 없이 이 책임을 나눴지만, Repository 클래스가 없다는 이유만으로 구조의 뎁스가 줄었다고 보지는 않습니다. 다음 페이지 규칙·중복 제거·오류 표시 정책과 Room 구독을 Soil로 감싼 비용은 여전히 앱의 몫입니다.

`SearchBooksQueryKey`는 `InfiniteQueryKey<SearchPage, Int>` 구현체이며 순수 식별자는 `SearchBooksQueryId`다. QueryKey는 독립 아키텍처 레이어 이름이 아니라 데이터 계층 구성 요소다. **ViewModel → Repository → API**와 **Presenter → QueryKey → API**는 책임 경계가 비슷하다는 개념적 비교이며, 실제 실행 경로 전체를 뜻하는 단순 호출 순서로 단정하지 않는다. Key에 요청·변환 책임이 남고 Soil이 실행 상태를 맡는 것이 이 선택의 핵심이다.

### 핵심 확인 — isLoading/isSuccess/isError를 직접 관리하지 않았나요?

**실제 패턴은 2번, Soil → 불변 UiState 투영이다.** Screen이 Soil 객체를 직접 렌더링하는 1번 방식도, 별도 mutable 서버 상태를 중복 갱신하는 3번 방식도 아니다.

| 확인 지점 | 실제 코드 | 의미 |
| --- | --- | --- |
| UI 모델 | `SearchUiState.content: SearchContent`, `Loading/Error/Empty/Results`, Results의 `isLoadingMore/loadMoreError` (SearchPresenter 34~56행) | 화면용 상태 타입과 필드는 존재한다. “로딩·오류 UiState를 전혀 정의하지 않았다”는 설명은 부정확하다 |
| 서버 상태 소유자 | 조건별 `rememberInfiniteQuery`, Soil query 객체 (96~108행) | Soil이 실행·캐시·누적 결과·로딩·오류 상태를 관리한다. fetch의 Retrofit 호출·변환·요청 정책은 데이터 계층 QueryKey에 남는다 |
| 변환 | `content = query.toContent()` (125~132행), `toContent()` (158~180행) | query 객체 타입·`fetchStatus`·`data`·`error`에서 매번 파생한다. 별도 mutable loading/error/results 저장소를 갱신하지 않는다 |
| 초기 요청·실패 | LoadingObject → Loading, LoadingErrorObject → Error. 재시도 Fetching 중에는 Loading | API 호출 전후로 앱이 loading=true/false를 수동 설정하지 않는다 |
| 추가 로딩·재조회 | Success/RefreshError의 기존 data를 유지하고 Fetching을 `isLoadingMore`로 변환 | 추가 요청과 기존 페이지 refresh가 이 표시에 함께 매핑된다. `isLoadingMore` 이름만으로 append 전용 상태라고 설명하지 않는다 |
| 재시도 | 실패 페이지가 다음 param이면 loadMore, 기존 페이지 실패면 refresh (112~120행) | Soil의 오류 타입만으로 실패 페이지를 모두 구별하지 못해 앱이 페이지 번호를 함께 기록한다 |
| UI 소비 | SearchScreen 110~151행의 content 분기·footer | Screen은 Soil 타입을 알지 않고 불변 화면 모델을 표시한다 |

별도로 mutable인 것은 `SearchSavedState`의 입력·확정 검색어·정렬(69~75, 90행), `FavoriteToggler`의 pending 명령·실패 알림이다. 후자는 로컬 쓰기 UX이며 검색 서버 요청 상태를 중복 관리하는 것은 아니다. 목록 스크롤은 Screen의 saveable 상태다.

본인이 줄이고 싶었던 것은 API 호출을 둘러싼 `isLoading=true → 호출 → finally에서 false`, 실패 시 `isError=true` 같은 수동 상태 전환이다. 현재 검색 구현은 그 전환을 Soil에 맡기므로 이 도입 목적에 부합한다. 화면용 상태 필드가 있다는 사실과 요청 상태를 직접 갱신한다는 것은 다르다.

따라서 보일러플레이트를 줄인 범위는 **서버 요청의 상태 전이·캐시·페이지 누적 관리**다. `SearchContent`와 변환·빈 결과·footer·재시도 정책까지 없앴다는 뜻은 아니다. 블로그의 `SoilDataBoundary`를 통한 직접 loading/error/content 경계 패턴을 과제에 그대로 적용한 것도 아니다.

### 목적·실제 활용·한계

| 목적/기능 | 과제에서 실제 사용 | 한계·사용하지 않은 범위 |
| --- | --- | --- |
| 서버 상태와 캐시의 일관성 | 앱의 공유 `SwrCachePlus`, 검색어+정렬 typed ID, `staleTime=5.minutes` | 메모리 캐시다. 검색 결과를 디스크에 영속화하지 않았다. fresh 기간이 끝났다고 무조건 주기 요청하는 타이머는 아니다 |
| 무한 조회 | InfiniteQuery의 페이지 chunk·loadMore·select | 다음 페이지는 `is_end`/50 상한, 도서 중복 제거는 SearchPaging, 스크롤 트리거는 앱. Soil LazyLoad는 사용하지 않았다 |
| 실패·재시도 | `shouldRetry`에 앱 오류 분류, query 상태를 UI로 변환, 수동 Retry | 앱이 오류 문구·실패 페이지·목록 유지 정책을 책임진다. 성능·API 호출 감소율을 측정한 결과는 없다 |
| 로컬 데이터의 일관된 구독 | Subscription → Room Flow로 ID·목록·개별 도서를 읽음 | Room이 단일 데이터 기준. 직접 Flow 구독도 가능하며 감싸는 계층의 비용이 있다 |
| 로컬 쓰기 | Mutation → DAO, 공통 `MutationId("favorite")` actor; pending/실패는 화면 Toggler | 서버 mutation/서버 query 무효화 용도가 아니다. DB 반영 후 하트가 갱신되므로 optimistic 하트 변경을 구현했다고 말하지 않는다 |
| Android 환경 대응 | AndroidMemoryPressure·AndroidNetworkConnectivity를 client policy에 전달 | WindowVisibility·주기 polling·검색 cache persistence를 별도 구성하지 않았다. 모든 자동 재검증 옵션을 실기기에서 검증했다는 주장도 없다 |
| 같은 선언 방식 | Query/InfiniteQuery/Subscription/Mutation이라는 API 체계가 선택 이유 | 실제 원격 조회는 InfiniteQuery이며 독립 단건 Query는 사용하지 않았다 |

### 꼬리질문 — Paging·Room·블로그와의 차이

- Soil은 TanStack Query의 직접 포팅인가요? → 공식 문서는 TanStack Query·SWR·RTK Query에서 영감을 받았다고 설명한다.
- Paging 3를 추가하지 않은 이유는요? → 서버 상태의 소유자를 하나로 유지하고 과제의 단방향 요구를 충족하려 했다. Paging 3의 maxSize 페이지 drop·anchor refresh·RemoteMediator는 별도의 장점이다. “무겁다”는 추가 구조 비용이며 측정된 성능 열세가 아니다.
- 2025 블로그에서는 Room과 Soil을 함께 쓰지 않았는데요? → 당시 동기화 지연을 관찰하고 롤백했으며 원인은 추정으로 남겼다. 이번 과제는 구독자가 없는 사이의 갱신과 재구독을 고려해 `keepAliveTime=Duration.ZERO`로 Room Flow를 다시 열고, 구독 사이 쓰기 반영을 확인하는 테스트를 작성했다. 과거 추정을 확정된 라이브러리 결함으로 말하지 않는다.
- “로컬 DB에는 캐시·재시도가 의미 없다”는 일반론인가요? → 당시 사례의 판단이다. 로컬 데이터도 비싼 조회·일시 실패·동기화 등의 상황에 따라 정책이 필요할 수 있다. 이번에는 원격 캐싱과 로컬 구독·쓰기의 목적을 구분한다.
- DroidKaigi 2026을 그대로 복사했나요? → 아니다. 자체 FIR 규칙·ScreenChannel·MutationTag·영속 query helper는 도입하지 않았다. 화면별 mutation ID 대신 공통 actor로 DB 명령 순서를 처리하고 UI 진행·실패를 Toggler로 나눴다. 검색 query는 조건을 가진 Presenter에서 연결한다.

### 근거·미확인

본인의 [Soil Query 적용해보기](https://velog.io/@mraz3068/Soil-Apply)와 [DroidKaigi 2025·2026 비교](https://velog.io/@mraz3068/Same-Soil-Different-Architecture-DroidKaigi-2025-2026-App-Comparison) 본문 전체를 읽고 실제 과제와 대조했다. 과거 토이 앱의 Ktor·Hilt·Boundary 구조를 현재 Retrofit·Metro·UiState 투영 구조의 성과로 섞지 않는다. 공식 [Soil 소개](https://docs.soil-kt.com/guide/what-is-soil)도 확인했다.

확인 기준: 제출 `f9f6b2290199b354eb2cb79f998ef4147b063b17`, 기존 조사 main `510d7a601402c00a2caed55f602be59e2738d990`. 두 기준의 SearchPresenter와 FavoriteSubscriptionKeys는 동일하다. QueryKey 책임은 최신 main `7e0479d0f1bf77f80378c40762637027615437a8`의 SearchBooksQueryKey와 SearchPresenter로 재확인했다. 제출 후 Writer 제거는 Q8에 분리한다. 이번 면접 노트 작업에서는 코드를 읽었으며 빌드·테스트·비교 측정을 실행하지 않았다.

- [SearchPresenter — query→UiState·retry](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchPresenter.kt#L96)
- [SearchScreen — 상태·footer 표시](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchScreen.kt#L110)
- [검색 query key·옵션](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/core/data/src/main/kotlin/io/github/easyhooon/booksearch/core/data/SearchBooksQueryKey.kt)
- [최신 SearchBooksQueryKey — ID·fetch·정책](https://github.com/easyhooon/book-search-android/blob/7e0479d0f1bf77f80378c40762637027615437a8/core/data/src/main/kotlin/io/github/easyhooon/booksearch/core/data/SearchBooksQueryKey.kt)
- [Room Subscription·keepAliveTime](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/core/data/src/main/kotlin/io/github/easyhooon/booksearch/core/data/FavoriteSubscriptionKeys.kt)
- [구독 사이 쓰기 반영 테스트](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/core/data/src/test/kotlin/io/github/easyhooon/booksearch/core/data/FavoriteSubscriptionKeysTest.kt#L173)

## Q7. Room Flow를 왜 Subscription으로 감쌌나요?

### 30초 답변

원격 데이터와 로컬 데이터를 Presenter에서 처리하는 방식을 일관되게 유지하려고 Room Flow를 Subscription으로 감쌌습니다. Presenter가 소스별 구독 방식을 다르게 알기보다 같은 방식으로 상태를 받도록 한 선택입니다. 다만 Room Flow를 직접 구독해도 요구사항은 해결할 수 있고 그쪽이 더 단순합니다. 이번에는 기존 서버 상태 처리 흐름과의 일관성을 우선했습니다.

### 꼬리질문

- 감싼 계층이 실제로 줄인 복잡도는 무엇인가요?
- Flow 직접 구독으로 바꾼다면 어디를 바꾸면 되나요?
- 로컬 상태를 서버 캐시와 혼동하지 않도록 어떻게 나눴나요?

### 근거·미확인

Subscription이 필수거나 직접 구독보다 항상 우월하다고 주장하지 않는다.

## Q8. FavoriteWriter를 왜 만들었고, 제출 후 왜 제거했나요?

### 30~45초 답변

처음에는 화면 이동 중 저장 취소를 막으려고 쓰기 책임을 분리했습니다. 제출 후 흐름을 다시 검토하니 Toggler와 공통 Mutation actor가 이미 정상적인 화면 이탈과 요청 순서를 처리하고 있어 Writer의 보호가 일부 겹쳤습니다. 그래서 화면 이탈·연속 변경·실패 후 복구 테스트와 결함 주입으로 검증한 뒤 Writer를 제거했습니다. 제출본에는 남아 있고, 저장소에는 이후 단순화한 버전을 반영했습니다.

### 설명 — 제출본과 개선본

- 제출본 `f9f6b2290199b354eb2cb79f998ef4147b063b17`: Toggler→Mutation→Writer→DAO. Writer의 전용 앱 Scope·Mutex가 있다. 제출 ZIP·APK는 이후 변경하지 않았다.
- 제출 후 개선본: Toggler→Mutation→DAO. Writer와 전용 ApplicationCoroutineScope·Mutex를 제거했고 다른 운영 클래스에 옮기지 않았다. 공통 `MutationId("favorite")` actor가 명령 순서를 처리한다.
- Toggler는 새 요청 접수를 닫은 뒤 pending·대기 명령을 완료할 때까지 참조를 유지하고 `job.complete()`로 정리한다. 일반적인 pop과 actor 자체 취소는 다르다.
- 책임이 일부 겹친 것이지 보장이 동일했던 것은 아니다. actor 자체가 취소돼도 독립 앱 Scope에서 쓰기를 완료하는 추가 보장은 의도적으로 내려놓았다. 프로세스 종료 중 미완료 쓰기는 두 버전 모두 보장하지 않는다.
- SQLite 트랜잭션은 DB 원자성·쓰기 직렬화를 담당하지만 UI 이벤트 접수 순서나 코루틴 수명을 대신 보장하지 않는다.

불필요하게 깊어진 구조인지 다시 살펴보자는 문제 제기는 본인이 했고, AI와 함께 책임을 검토했다. 구현 변경·테스트 실행은 AI가 수행한 범위를 포함한다. 본인이 모든 코드·테스트를 직접 작성했다고 표현하지 않는다. 평가자가 지적해서 바꾼 이력도 아니다.

### 꼬리질문 — 취소·Scope·순서

- 왜 처음에는 겹침을 놓쳤나요? → 처음에는 쓰기 수명을 따로 보호하려 했고, 이후 Toggler의 대기 명령 처리까지 구조가 바뀌었습니다. 그 단계에서 전체 경로의 보호 범위를 끝까지 다시 검토하지 못했습니다. 제출 후 경로를 재검토하고 검증 범위를 보강했습니다.
- 도입 순서는요? → 977a558에서 수명 위험 사전 분석, 44316c2에서 Writer 구현, 2bad8fa에서 queued 명령 Toggler 보완. QA 실패 뒤 급히 도입한 것은 아니다. 이후 구조 변경에 맞춰 책임을 다시 평가했다.
- 제거 후에도 필요한 보호는요? → 정상 pop에서 접수한 명령을 완료할 때까지 Toggler 참조를 유지하고, 화면 간 같은 Mutation actor로 명령 순서를 처리한다.
- 테스트가 무엇을 증명하나요? → 느린 저장·빠른 해제의 최종 DB 상태, 같은 프레임 접수·pop과 대기 명령 완료, 실패 후 후속 쓰기, Room 관찰을 검증했다. 저장 누락·pop 취소·actor 분리 결함을 넣었을 때 관련 테스트 실패도 확인했다. 모든 취소·기기 동작을 보장하는 것은 아니다.
- actor 자체가 취소되면요? → DAO도 취소될 수 있다. 이전 Writer의 독립 완료 보장은 제거한 트레이드오프다. 정상 화면 pop에서는 Toggler가 완료까지 참조를 유지하는 범위를 검증했다.
- Mutex 대신 SQLite가 순서를 보장하나요? → DB 쓰기 직렬화와 UI 명령 순서는 별개다. 마지막 사용자 의도를 반영할 명령 순서는 공통 Mutation actor가 맡는다.
- Scope 설명이 바뀌었나요? → Writer의 앱 Scope는 제출본 설명이다. 개선본에는 Writer·전용 앱 Scope·Mutex가 없다. Toggler·Search 수명과 공통 actor의 수명을 구분한다.
- 취소를 오류로 삼키나요? → SearchBooksQueryKey와 FavoriteToggler에서 CancellationException을 다시 던진다. runSuspendCatching은 사용하지 않는다.
- 프로세스 종료도 견디나요? → 어느 버전도 종료 중 미완료 쓰기의 완료를 보장하지 않는다.

### 근거·미확인

제출 당시 도입 커밋·Scope 설명은 기존 본인 설명에 근거하며 977a558에는 분석 문서만 있었다. 제출 후 변경은 [PR #2](https://github.com/easyhooon/book-search-android/pull/2), [검증 코멘트](https://github.com/easyhooon/book-search-android/pull/2#issuecomment-6107392839), [Writer 제거 검증 문서](https://github.com/easyhooon/book-search-android/blob/2722737d6648f9071cd80bb48749e0ceb864b38d/docs/WRITER_REMOVAL.md)를 인증된 조회로 확인했다. 병합 main은 `2722737d6648f9071cd80bb48749e0ceb864b38d`, 검증 head는 `0ab5a46d7f418056e6bfaa920a36184cfd023ae7`이다.

보고된 검증은 기준 140개→145개 테스트, 실패·오류·skip 0, APK 빌드·lint 통과(오류0·경고2)다. 세 임시 결함을 검출하고 원복한 뒤 전체 검사가 통과했다. 이는 보고 문서 확인이며 면접 노트 작업에서 테스트를 다시 실행한 것은 아니다. 실기기 재검증·CI 실행·제출 패키지 재생성은 없었다. 사용성 개선 측정이나 평가자 피드백·탈락 사유를 근거로 하지 않는다.

## Q9. 운영 중 어려운 문제를 해결한 경험이 있나요?

### 30초 답변

Hi-me에서 특정 기기는 사진을 찍고 돌아오면 앱이 재시작된 것처럼 보이고 업로드가 중단됐습니다. Fatal 로그가 없어 앱 종료와 WebView Renderer 종료를 나눠 추적하고, 메모리와 WebView 정보를 추가해 메모리 압박이 원인임을 확인했습니다. 이후 WebView만 복원하고 촬영 요청과 결과를 보관했다가 브릿지가 준비되면 다시 전달하도록 바꿔, Renderer가 종료돼도 사진 업로드를 복구할 수 있게 했습니다.

### 꼬리질문

- Fatal 로그가 없다는 사실에서 무엇을 추론했나요?
- pending state와 request id·TTL은 각각 무엇을 해결하나요?
- 복원 뒤 중복 전달·오래된 요청은 어떻게 구분했나요?

### 근거·미확인

PORTFOLIO.md의 'WebView Renderer 종료 후 사진 업로드 흐름 복구', CV.md의 Hi-me 사례. onRenderProcessGone에서 WebView 버전·URL·가용 메모리·didCrash를 Non-Fatal로 수집. ViewModel pending state와 TTL localStorage, bridge-ready 재전달을 문서가 명시한다. 성공률·재발률·검증 기기 수는 없다. 회사 비공개 근거는 접근이 막혀 기존 문서 진술이다. 2026-07-30 d0c4154 포트폴리오에도 같은 사례가 있으나 실제 제출본 여부는 미확인.

## Q10. 대시보드 성능을 어떻게 개선하고 검증했나요?

### 30초 답변 — 확인된 범위

세컨드 윈드에서 Semaphore permit이 1이라 API가 하나씩 실행되는 병목을 독립 API의 병렬 실행으로 바꿨습니다. 이때 여러 요청이 동시에 토큰을 갱신하려는 경합을 막기 위해 싱글플라이트 패턴도 적용했습니다. Health Connect 데이터는 유형별로 병렬 처리했습니다. 기존 측정 기록상 첫 데이터 준비는 2.835초에서 1.116초로 약 60.6%, 최초 동기화 완료는 6.546초에서 4.740초로 약 27.6% 줄었습니다.

### 꼬리질문 — 싱글플라이트

Q. 싱글플라이트가 무엇인가요?

동일 키의 요청이 동시에 들어오면 실제 작업은 한 번만 실행하고, 나머지 요청은 그 진행 중 작업의 동일한 결과를 기다리는 방식입니다. 서로 다른 키는 별개 작업으로 다룰 수 있습니다. 핵심은 중복 동시 작업을 합치는 것입니다.

Q. 캐시·Mutex와 무엇이 다른가요?

- 캐시: 이미 완료된 결과를 다시 사용한다.
- 싱글플라이트: 아직 진행 중인 작업을 공유한다.
- Mutex만 사용: 한 번에 하나씩 실행하도록 순서를 정한다. 대기한 호출이 각각 같은 작업을 다시 실행할 수 있으므로 그 자체로 중복 요청을 합치지 않는다.

공식 정의 근거: [Go singleflight Group.Do](https://pkg.go.dev/golang.org/x/sync/singleflight#Group.Do). Go API는 개념 정의 근거이며 Kotlin 구현에 이 패키지를 사용했다는 뜻이 아니다.

Q. 본인 대시보드에도 싱글플라이트를 적용했나요?

본인의 설명에 따르면 Semaphore permit 1의 API 직렬 병목을 병렬 실행으로 바꾸면서 토큰 refresh 경합을 막기 위해 싱글플라이트 패턴을 적용했습니다. 기존 이력서에는 병목 제거와 유형별 병렬화만 명시되어 있어 싱글플라이트 적용은 추가 본인 진술로 구분합니다. 본인은 synchronized를 사용한 것으로 기억하지만 아직 코드로 확정하지 않았습니다. 실제 키·공유 결과/완료 대기 방식·공유 Deferred 여부·정리/오류/취소 동작도 미확인입니다.

Q. 왜 Mutex 대신 synchronized를 사용했나요?

OkHttp의 Authenticator.authenticate는 suspend가 아니라 Request?를 반환하는 동기 콜백이라, 모니터 락으로 진입을 제어하는 것이 단순한 선택이었습니다. Mutex는 기다리는 코루틴을 suspend할 수 있지만 synchronized는 기다리는 스레드를 block합니다. 이 동기 콜백에서 Mutex를 runBlocking으로 감싸더라도 호출 스레드의 대기는 남습니다. 다만 락 자체는 직렬화만 합니다. 락에 진입한 뒤 다른 요청이 이미 토큰을 갱신했는지 다시 확인하고 최신 토큰을 재사용하는 처리가 중복 갱신 방지의 핵심입니다.

위 답변은 동기 Authenticator에 대한 선택 이유를 설명하는 초안입니다. 본인 구현에서 Authenticator·synchronized·락 내부 토큰 재확인을 실제 사용했는지는 코드 확인 전 미확인으로 유지합니다. 긴 네트워크 작업을 락 안에서 수행한다면 대기 스레드가 생기는 비용도 인정합니다. Mutex의 코루틴 친화성이나 synchronized의 단순함을 일반적인 성능 우열로 말하지 않습니다.

공식 근거: [OkHttp Authenticator 소스](https://github.com/square/okhttp/blob/master/okhttp/src/commonJvmAndroid/kotlin/okhttp3/Authenticator.kt), [kotlinx.coroutines Mutex](https://kotlinlang.org/api/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.sync/-mutex/). authenticate의 nullable Request 반환은 재요청을 포기할 수 있는 경로이며, 중복 refresh와 무한 인증 재시도는 별개입니다. 후자는 refresh 실패 시 중단·시도 제한 등의 처리가 필요합니다.

Q. 싱글플라이트면 무한 토큰 refresh나 401 재시도가 모두 해결되나요?

동시 refresh 경합을 합치는 것과 401 재시도 루프를 제한하는 것은 별개입니다. lock 안에서 토큰을 다시 확인하는지, refresh 실패를 어떻게 전달하는지, 재시도 상한이 있는지는 실제 코드 확인이 필요합니다. 싱글플라이트 하나만으로 모든 무한 재시도를 막는다고 말하지 않습니다.

### 꼬리질문 — 측정·병렬화

- 두 시간의 시작·종료 이벤트는 각각 무엇인가요?
- 측정 기기·OS·네트워크·데이터량·표본 수·중앙값/평균·cold/warm 조건은 무엇이었나요?
- 제거한 전역 세마포어의 보호 대상은 무엇이며 필요한 동시성 제한은 어디에 남겼나요?
- 병렬화 후 오류·취소·Health Connect 제한은 어떻게 처리했나요?
- 동일 요청 합치기와 서로 다른 데이터 유형 병렬화는 어떻게 다른가요?

### 근거·미확인

RESUME.md:47, 추가 커밋 e16c2e085f17dab7d36cb68ba6e6c6685f80a04b (2026-08-07). 2026-07-30 d0c4154 이력서에는 이 수치가 없다. 계산은 (2.835-1.116)/2.835≈60.63%, (6.546-4.740)/6.546≈27.59%로 문서 반올림과 일치한다. 현재 문서는 첫 대시보드 '데이터 준비'와 최초 '동기화 완료'를 구분하며 렌더/FPS/앱 시작 전체 시간으로 일반화하지 않는다.

이 진술에서 확정하는 범위는 Semaphore permit 1 직렬 병목→독립 API 병렬화와 refresh 경합 방지 패턴 적용이다. 본인이 '발생할 수 있는' 위험과 해결을 설명한 것이므로 실제 운영에서 무한 refresh가 발생했다거나 장애 횟수가 있었다고 추정하지 않는다. 잠재 위험을 다룬 설명과 실제 발생 기록을 구분한다. 후속 진술로 synchronized를 사용한 것으로 기억한다고 했으나 코드 확인 전 확정하지 않는다. 토큰 재확인·refresh 실패 처리·재시도 상한도 미확인이다.

회사 PR 원문·측정 로그는 확보하지 못했다. 측정 조건·원본 코드·최신 브랜치 검증 전 독립 검증된 벤치마크로 말하지 않는다. 실제 코드의 싱글플라이트 세부 구현은 미확인이며 현재 근거는 기존 이력서와 본인 설명이다.

## Q11. 이전에도 같은 과제를 제출했는데, 이번에는 무엇을 바꿨나요?

### 30~45초 답변

예전에 같은 회사의 도서 검색 과제를 제출했고 탈락 후 사유를 문의했던 기억이 있습니다. 당시에는 ViewModel과 Repository, 직접 만든 페이지네이션을 사용했고 테스트는 작성하지 않은 것으로 기억합니다. 이번에는 제 설계 관점을 보여주고 싶은 마음도 있었지만, 낯선 기술을 쓰는 것 자체보다 상태의 책임과 수명, 오류와 취소를 설명할 수 있는 구조를 만드는 데 집중했습니다. 과거 결과의 원인을 단정하기보다 이번 선택과 검증 범위를 구체적으로 설명하겠습니다.

### 설명

과거 구현에 익숙한 구조를 썼다는 사실과 이번 구조가 더 낫다는 결론은 별개다. 지금 보여줄 것은 선택 이유·대안·사용자 흐름·검증 범위다. 개인의 설계 취향은 출발점일 수 있지만 요구사항과 비용으로 설명해야 한다.

### 꼬리질문

- 지난 탈락 사유가 버그였나요? → 실제 피드백·제출 스냅샷을 확보하지 못해 확정할 수 없다.
- 현재 BookSearch main이 당시 제출 코드인가요? → 이후 블로그·연습용 변경이 포함될 수 있어 동일하게 취급하지 않는다.
- 이번에는 어떤 검증을 추가했나요? → 작성한 테스트와 실행 기록·미검증 범위를 구분해 Q14의 근거로 답한다.

### 근거·미확인

과거 제출·탈락·문의 및 당시 구조와 테스트 미작성은 본인의 기억이다. 과거 제출 커밋·구체적 버그·실제 탈락 사유는 미확인이다. 현재 main에서 옛 코드를 역추정하거나 '버그 때문에 탈락했다'고 쓰지 않는다. 이번 정리는 기존 코드를 제거하거나 수정한 작업이 아니다.

## Q12. retain·Soil·Metro가 낯설어서 후임 유지보수가 어렵지 않나요?

### 30~45초 답변

맞습니다. 익숙한 권장 패턴은 온보딩에 유리하고, 제가 선택한 구조는 라이브러리 학습과 업데이트 비용이 있습니다. 다만 익숙한 구조만이 정답이라고 생각하지는 않습니다. 이번에는 Presenter에서 상태와 이벤트를 조합하고, 요청 상태는 Soil, 객체 수명은 retain, 의존성 조립은 Metro로 나눴습니다. 문서만으로 비용이 사라졌다고 보지는 않습니다. 실제 팀 도입이라면 팀의 이해도와 작은 기능 검증을 기준으로 결정하고, 이점보다 비용이 크면 익숙한 구조를 선택하겠습니다.

### 설명 — 구체적 가치와 비용

- 가치: 입력→확정 검색 조건→query→UI 모델이라는 흐름을 한 Presenter에서 따라갈 수 있다. 요청·캐시 상태와 UI의 저장 상태를 중복 소유하지 않고, 변경 가능한 화면 상태와 데이터 규칙의 경계를 드러내려는 선택이다.
- 비용: retain의 제거·정리 규칙, Soil의 query 상태·재시도 계약, Metro 그래프·컴파일러 호환성을 배워야 한다. 라이브러리 업데이트·버그 분석·팀 리뷰의 비용도 남는다. 문서량이나 테스트 수만으로 후임 유지보수가 쉽다고 결론 내리지 않는다.
- 실제 팀 도입 계획: 한 기능의 데이터·이벤트 흐름 예시를 동료와 함께 따라가고 작은 변경을 해본다. 수명·취소·저장 복원 규칙과 회귀 테스트를 검토하고, 이해하기 어려운 경계는 줄인다. 업그레이드·빌드 환경 비용까지 평가한 뒤 도입 여부를 결정한다. 이는 향후 계획이며 이미 팀 검증을 했다는 주장이 아니다.

### 꼬리질문

- 문서가 있으면 온보딩 비용은 해결되지 않나요? → 문서는 탐색을 돕지만 이해·변경·디버깅 비용은 실제 작업으로 확인해야 한다.
- 구체적인 흐름 하나를 설명해보세요. → SearchPresenter가 입력·확정 검색어·정렬을 저장 상태로 관리하고 확정 조건의 Soil key를 만든다. Room에서 관찰한 즐겨찾기 ID는 Root가 전달하고, UI 이벤트는 쓰기 명령으로 연결한다.
- 데이터 일관성의 기준은 어디인가요? → 즐겨찾기의 기준은 Room이다. Metro나 retain을 데이터 저장소로 삼지 않는다.
- 더 익숙한 구조로 바꾸면 무엇을 유지하나요? → 데이터 단일 기준, 이벤트·쓰기 계약과 회귀 테스트를 유지하고 상태 소유자를 바꿀 수 있다. 전환을 실제로 수행·검증한 것은 아니다.
- Kotlin·JDK 업데이트 비용도 있나요? → 보관 문서에 Metro 실행 JVM 때문에 JDK 21이 필요하며 원문의 JDK 17 조건과 차이가 남는다고 기록되어 있다. 편의만 설명하지 않는다.

### 근거·미확인

Writer 제거 전 과제 보관본의 ARCHITECTURE, SearchPresenter, FavoriteWriter, 수명·재시도 테스트 파일을 읽어 대조했다. Root/Presenter/Screen 경계, 일반 Kotlin ID·가격 규칙, 제출본의 앱 범위 쓰기와 Mutex, retain·저장 복원의 구분은 확인된다. Writer·전용 앱 Scope·Mutex는 제출 후 PR #2에서 제거되었으므로 현재 main의 구조로 설명하지 않는다(Q8). 공식 근거는 [retain 수명](https://developer.android.com/develop/ui/compose/state-lifespans), [Soil 소개](https://docs.soil-kt.com/guide/what-is-soil), [Metro 프로젝트](https://github.com/ZacSweers/metro).

후임의 온보딩 시간, 실제 팀 채택·업데이트 경험, 장기 유지보수 비용 감소는 미확인이다. 테스트·문서 존재를 팀 유지보수 검증 완료로 표현하지 않는다. Circuit만의 논의로 한정하지 않으며 이 과제에는 Circuit을 도입하지 않았다.

## Q13. Compose를 화면 외에 상태 관리에 활용한다는 뜻은 무엇인가요?

### 30~45초 답변

Compose UI는 배치와 그리기, 입력을 담당하지만 Runtime은 상태 관찰과 Composition의 실행 기반이고 Compiler는 Composable 함수를 그 기반에 맞게 변환합니다. 저는 이를 화면만이 아니라 상태를 조합하는 데도 활용하고 싶어서 얇은 Composable Presenter를 선택했습니다. retain은 객체 수명, Soil은 요청과 캐시 상태, Metro는 의존성 조립을 맡깁니다. 모든 도메인 로직을 Composable에 넣자는 뜻은 아니고, 독립 규칙은 일반 Kotlin에 두었습니다. ViewModel로도 이런 책임 분리는 가능합니다.

### 설명 — 책임과 제한

| 구성 | 이 과제에서 맡긴 책임 | 대신하지 않는 것 |
|---|---|---|
| Compose UI | 레이아웃·그리기·입력과 사용자 이벤트 전달 | 도메인 규칙·영구 저장 |
| Runtime / Compiler | 상태 관찰·Composition 실행 기반 / Composable 변환과 최적화 지원 | 앱별 데이터 계약·스레드 안전성·전체 아키텍처 결정 |
| Composable Presenter | 상태 출처를 UI 모델로 조합하고 이벤트를 명령에 연결 | 모든 비즈니스 로직·순수 규칙의 구현 장소 |
| retain | 선택한 범위에서 일반 객체 유지 및 정리 | 프로세스 종료 뒤의 영구 복원·자동 Scope 설계 |
| Soil | query·cache·비동기 요청 상태 | 앱의 모든 로컬 상태와 데이터 일관성 정책 |
| Metro | 컴파일 시 의존성 그래프와 factory 조립 | UI 상태·Room 데이터의 기준·수명 정책 자동 결정 |

검색 조건의 저장과 query 객체 유지, 진행 중 쓰기의 수명은 다른 계약이다. 독립 ID·가격 규칙은 일반 Kotlin 함수로 분리하고 Presenter에서는 이벤트·상태 연결만 수행하는 방향이다.

### 꼬리질문

- ViewModel은 Compose와 맞지 않나요? → 아니다. ViewModel은 유효한 상태 소유자이며 Scope·SavedState·DI 통합 등 장점이 있다. Q5의 선택은 특정 목표·범위에 대한 판단이다.
- Composable 함수이면 UI를 반드시 그리나요? → 꼭 그렇지는 않다. 여기서는 상태를 조합해 UI 모델을 반환하는 Presenter를 사용한다.
- retain이 상태 저장·복원을 모두 해주나요? → 아니다. 구성 변경의 객체 유지와 프로세스 복원을 분리한다.
- 순수 도메인 규칙도 Composition에 묶었나요? → 아니며 실제 코드의 ID·가격·페이지 규칙 분리를 예로 든다.

### 근거·미확인

공식 [Compose Runtime](https://developer.android.com/jetpack/androidx/releases/compose-runtime)의 UI·Runtime·Compiler 역할 설명, [Compiler 설정](https://developer.android.com/develop/ui/compose/compiler), Q5·Q12의 1차 자료를 참고했다. 과제 보관본 SearchPresenter의 Composable 상태 조합과 일반 Kotlin 모델 규칙을 대조했다. 특정 개발자의 권위를 선택 근거로 삼지 않으며 출처 없는 발언을 인용하지 않는다. ViewModel보다 성능·유지보수성이 우월하다는 비교 측정은 없다.

## Q14. AI를 허용한 과제에서 본인의 판단을 어떻게 보여주나요?

### 30~45초 답변

AI가 작성한 양보다 제가 어떤 선택을 했고 어떻게 확인했는지를 보여주려 합니다. 설계 초안과 구현·테스트 작성에 AI를 활용했지만, retain 기반 수명과 Soil의 책임, 저장·복원 경계 같은 선택은 대안과 비용을 보고 결정했습니다. 코드에서 상태와 이벤트 흐름을 설명하고 테스트·실기기 기록으로 확인한 범위를 제시하겠습니다. 이전 빌드의 QA와 최종 코드 검증을 섞지 않고, 설명하지 못하는 코드나 아직 확인하지 못한 부분은 따로 인정하겠습니다.

### 설명 — 판단을 보여주는 예

- 채택·수정: ViewModel 중심 초안 대신 retain을 선택한 이유, Retrofit 선택과 단순 전달 Repository 생략 이유, 상세 스냅샷 복원과 제출본의 앱 범위 쓰기 제한을 설명한다. 제출 후에는 중복 보호를 검토해 Writer를 제거한 판단과 내려놓은 보장도 구분한다(Q8).
- 대안·비용: 직접 Room Flow 구독도 가능하고, Paging 3와 ViewModel의 장점도 인정한다. 덜 익숙한 구조가 항상 좋다는 식으로 답하지 않는다.
- 검증: 어떤 실패·상태 전이를 확인하는 테스트인지 실제 파일과 기록을 연결한다. Fake DAO의 지연·취소 검증을 실제 기기 Room 오류 재현으로 바꾸어 말하지 않는다.
- 한계: 해당 회사가 AI 사용자를 어떻게 채점하는지는 모른다. AI 미사용자의 판단이나 역량을 낮추지 않는다.

### 꼬리질문

- AI가 제안했지만 바꾼 결정 하나는요? → AI_USAGE의 선택 표와 실제 코드가 일치하는 사례를 들고, 대안·비용을 함께 설명한다.
- 테스트도 AI가 작성했다면 무엇이 본인 판단인가요? → 어떤 위험을 검증할지, 기대 결과가 맞는지, 실행·로그가 무엇을 보장하는지 판단한 책임이다.
- 모든 검증이 완료됐나요? → 아니다. 기록별 대상·빌드와 최종 판정을 구분한다. 아래 확인 범위 이상으로 답하지 않는다.
- 설명하지 못하는 코드가 나오면요? → 먼저 미이해를 인정하고 계약·호출 흐름·테스트를 확인한다. 이미 전 코드를 이해했다고 단정하지 않는다.

### 근거·미확인 — 이번 읽기 확인 범위

Writer 제거 전 보관본의 AI_USAGE, ARCHITECTURE, QA와 SearchPresenter·FavoriteWriter 및 테스트 파일을 가볍게 대조했다. 구현이나 테스트는 이번 면접 노트 작업에서 재실행하지 않았다. 이후 Writer 제거는 별도 PR #2의 보고를 확인했으며 제출 ZIP은 변경하지 않았다(Q8).

- QA에는 자동 테스트 140개 실패·오류·건너뜀 0, APK·Studio 가져오기·제출 ZIP 검증 통과가 기록되어 있다. 이번 작업에서 원본 실행 로그까지 독립 재검증한 수치는 아니다.
- 제출 후 Writer 제거 검증은 145개 테스트와 결함 주입 검출·원복 후 통과, APK·lint 통과 기록이다. 기존 140개 기록과 구분하며 이 변경의 실기기 재검증·CI 실행은 없다.
- Writer 제거 전 보관본 APK의 Galaxy 검색·상세·즐겨찾기·정렬·로컬 검색·가격 필터 확인이 기록되어 있다.
- 네트워크 오류·페이지네이션·앱 종료 후 복원·태블릿·폴더블의 해당 보관본 APK 재검증은 미실행으로 명시되어 있다. 기존 화면·이전 빌드 QA를 현재 코드의 통과 근거로 쓰지 않는다.
- AI_USAGE에는 최종 재검증 대기 문구가 남아 QA의 통과 기록과 상태 설명이 완전히 일치하지 않는다. 둘을 종합해 '전체 검증 완료'로 결론 내리지 않는다. 정확한 최종 제출본과 검증 대상은 추가 대조가 필요하다.

기존 Q4의 실기기 검증 언급은 검증 활동을 했다는 뜻이며 모든 복원·오류·기기 시나리오의 최종 통과를 의미하지 않는다. 현재 실제 제출된 파일과 동일한지는 이번 확인에서 확정하지 않았다.

## Q15. ADR이 무엇이고 왜 작성하나요?

### 30~45초 답변

ADR은 Architecture Decision Record, 아키텍처 의사결정 기록입니다. 어떤 문제와 제약 때문에 선택했는지, 대안은 무엇이었는지, 무엇을 결정했고 어떤 결과와 비용이 남는지를 적습니다. 나중에 선택을 바꾸거나 다른 사람이 유지보수할 때 배경을 이해하는 데 도움이 됩니다. 다만 문서가 길다고 설계가 좋은 것은 아니고, 실제 코드·테스트·현재 제약과 맞아야 합니다. 이번에는 아키텍처와 AI 활용 문서에 선택 이유와 비용을 남겼습니다.

### 설명

최소 구성은 배경/문제·대안·결정·결과와 비용이다. 상태(제안·채택·대체)와 선택을 바꿀 조건을 남기면 이후 결정 추적에 도움이 된다. 짧은 예로 retain 선택의 목표, ViewModel 대안, 직접 수명 관리 비용, 프로세스 복원의 별도 계약을 기록할 수 있다. 이는 설명 예이며 정식 ADR 파일을 새로 작성했다는 주장이 아니다.

### 꼬리질문

- 일반 설계 문서와 어떻게 다른가요? → 최종 구조뿐 아니라 특정 선택의 맥락·대안·결과를 추적하는 데 초점을 둔다.
- 이번에 정식 ADR을 작성했나요? → ARCHITECTURE·AI_USAGE에 의사결정 내용이 있지만 별도 ADR 체계나 파일 존재는 확인하지 않았다.
- 문서가 많으면 설계가 좋은가요? → 아니다. 변경에 필요한 판단을 설명하고 코드·검증 결과와 일치해야 한다.

### 근거·미확인

1차 참고: [Architectural Decision Records](https://adr.github.io/). 과제 문서의 최종 선택·비용·제약은 확인했지만 문서화로 온보딩 비용이 줄었다는 실측은 없다. 이 면접 노트는 기존 답변을 복사한 확정 기록이 아니라 본인 의도와 확인한 근거를 반영한 말하기 초안이다.

## Q16. 왜 CI/CD를 재설계했고 GitHub Actions를 선택했나요?

### 짧은 답변

Bitbucket에서 GitHub로 저장소를 이관하면서 기존 CI/CD를 그대로 사용할 수 없었습니다. 로컬에서 배포하는 방법도 있었지만, 배포 이력을 일관되게 남기고 팀에서 확인하기 어렵다고 판단했습니다. 그래서 GitHub Actions 기반으로 배포 구조를 재설계해 실행 기록을 남기는 방식을 선택했습니다.

### 설명

형상관리 이관이 재설계의 계기였다. 목적은 배포 이력을 일관되게 남기고 팀에서 확인할 수 있게 하는 것이었다. 로컬 배포도 대안이었으나 당시 팀의 기록·확인 요구를 고려해 GitHub Actions를 선택했다. 로컬 배포에서 이력을 남기는 것이 일반적으로 불가능하다는 뜻은 아니다.

### 꼬리질문

- 기존 이력 확인 방식과 변경 후 추적 가능한 정보는 무엇인가?

### 근거·미확인

Bitbucket→GitHub 이관, 기존 CI/CD 사용 불가 상황, 로컬 배포 대안 검토와 GitHub Actions 선택 이유는 본인의 직접 설명에 근거한다. 회사 워크플로·실행 로그를 독립 확인한 결과는 아니다.

기존 이력 확인 방식과 변경 후 추적 가능한 상세 항목은 아직 확인되지 않았다. 커밋·아티팩트·환경·승인·롤백 연결이나 배포시간 개선은 구현 완료 성과로 단정하지 않는다. 목적과 확인된 선택 이유를 실제 운영 상세와 구분한다.

## Q17. Molecule을 어떤 목적으로 사용했나요?

### 30초 답변

이 과제에서는 Molecule을 Composable Presenter의 상태 전이를 테스트하는 데만 사용했습니다. 화면을 그리지 않고 Presenter를 실행해 반환하는 UI 모델을 Flow로 받고, Turbine으로 이벤트 뒤 상태와 오류 처리를 확인했습니다. 일반 Kotlin 규칙은 일반 단위 테스트로 확인하고, Compose 상태와 효과가 필요한 부분에 Molecule을 썼습니다. UI 표시나 retain 수명, 프로세스 복원까지 검증해주는 도구는 아니어서 해당 테스트는 별도로 두었습니다.

### 설명 — 실제 의존성과 실행 방식

- 버전은 제출본과 조사 시점 main 모두 `molecule-runtime:2.2.0`이다. feature convention의 `testImplementation`과 테스트 전용 `core:testing` 모듈의 `api`로 선언한다. `core:testing/src/main`에 helper가 있지만 앱·feature에서는 이 모듈을 테스트 의존성으로만 연결한다. 앱 운영 경로의 Molecule 호출은 없다.
- `presenterFlow(client, presenter)`는 `moleculeFlow(RecompositionMode.Immediate)`로 Presenter의 반환 UI 모델을 **Flow**로 만든다. `launchMolecule`이나 StateFlow 출력 방식은 이 코드에서 사용하지 않는다.
- 검색·즐겨찾기·상세의 Presenter 테스트가 `presenterFlow`를 호출한다. `runTest`, MainDispatcherRule, 테스트용 Soil client·key와 Fake Mutation, Turbine의 `.test`·`awaitItem` 계열로 이벤트와 상태 변화를 확인한다. Android Compose Runtime의 Trace·Log 호출 때문에 Robolectric에서 실행하는 구성이다.
- `Immediate`는 Molecule이 즉시 clock을 구성하므로 테스트 코드에서 별도 화면 frame clock을 제공하지 않는다. 기기 화면 프레임을 기다리는 `ContextClock` 모드는 쓰지 않는다. Immediate도 Compose Runtime의 재구성을 사용하며 UI 렌더링 타이밍을 재현하는 것은 아니다.
- Soil의 CompositionLocal을 제공하는 helper는 `currentComposer.startProviders/endProviders`를 사용한다. 중첩 provider content만 재구성되면 바깥 Molecule 반환값의 방출이 누락될 수 있다는 코드 주석에 따라 같은 그룹에서 반환값을 얻는다. `InternalComposeApi`에 의존하는 만큼 업데이트·테스트 helper 유지 비용이 있다.

### 꼬리질문

- 왜 일반 단위 테스트로 안 되나요? → 순수 가격·ID·페이지 규칙은 일반 단위 테스트로 충분하다. 이 Presenter는 Composable이며 remember·상태 관찰·효과와 재구성이 필요해 일반 함수처럼 한 번 호출하는 것만으로 상태 전이를 확인할 수 없다. Molecule은 그 실행 환경을 제공하는 선택이고, Compose 테스트로 검증하는 대안도 있다.
- ViewModel보다 무조건 테스트가 쉬운가요? → 아니다. UI 모델 방출에 집중할 수 있지만 Composition·dispatcher·Soil key/fake 구성이 필요하고 내부 API helper 비용도 있다. ViewModel의 Flow도 코루틴 테스트로 검증할 수 있으며 비교 우월성은 측정하지 않았다.
- UI 테스트까지 대체하나요? → 아니다. 실제 레이아웃·입력·semantics·내비게이션은 Compose UI/호스트 테스트와 기기 QA 범위다. Molecule 테스트 통과로 화면 표시나 기기 동작까지 보장하지 않는다.
- retain과 프로세스 복원도 확인하나요? → Molecule 자체가 보장하지 않는다. 앱 NavHost의 retained store·백스택 제거·Activity 재생성은 별도 호스트 테스트, 실제 프로세스 종료·복원은 별도 기기 검증과 구분한다.
- 앱에서도 Presenter를 Flow로 바꿔 사용하나요? → 이 과제에서는 아니다. 실제 화면은 Composable Presenter를 직접 연결하며, Molecule Flow는 테스트 helper의 출력이다.

### 근거·미확인

제출 커밋 `f9f6b2290199b354eb2cb79f998ef4147b063b17`과 조사 시점 원격 main `6f80ef0c568626bcdb08d6a81d5229e214805774`의 소스 사본을 읽었다. 두 커밋의 PresenterFlow helper는 동일하며 Molecule 의존성·호출 범위도 위와 같다. 다른 작업 브랜치의 변경을 추정하지 않는다.

- [제출본 PresenterFlow](https://github.com/easyhooon/book-search-android/blob/f9f6b2290199b354eb2cb79f998ef4147b063b17/core/testing/src/main/kotlin/io/github/easyhooon/booksearch/core/testing/PresenterFlow.kt)
- [조사 main PresenterFlow](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/core/testing/src/main/kotlin/io/github/easyhooon/booksearch/core/testing/PresenterFlow.kt)
- [feature 의존성 설정](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/build-logic/src/main/kotlin/AndroidFeatureConventionPlugin.kt), [테스트 전용 모듈](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/core/testing/build.gradle.kts)
- [SearchPresenterTest](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/feature/search/src/test/kotlin/io/github/easyhooon/booksearch/feature/search/SearchPresenterTest.kt)
- [Cash App 공식 Molecule 2.2.0 README](https://github.com/cashapp/molecule/blob/2.2.0/README.md): Compose 상태를 Flow/StateFlow로 연결하며 Immediate 모드와 Turbine 기반 테스트를 설명한다. 프로젝트에서는 그중 Flow 방식을 사용한다.

이번 노트 작업은 의존성·코드 읽기 확인이며 빌드나 테스트를 재실행하지 않았다. StateFlow의 일반 지원과 과제의 실제 Flow 사용을 구분하고, 테스트 속도·유지보수성 개선 수치는 주장하지 않는다. 제출 코드·ZIP은 변경하지 않았다.

## Q18. Turbine은 왜 사용했고 Molecule과 어떤 차이가 있나요?

### 30초 답변

Molecule이 Composable Presenter를 실행해 Flow를 만들면, Turbine은 그 Flow에서 나오는 상태를 기다리고 확인하는 역할입니다. 임의로 시간을 기다린 뒤 마지막 값만 보기보다, 이벤트를 보내고 필요한 상태가 나왔는지 확인하려고 사용했습니다. 다만 재구성으로 생기는 중간 방출 수에 테스트를 묶지는 않았고, 조건에 맞는 상태를 기다렸습니다. 일반 Flow도 Turbine 없이 테스트할 수 있지만, 구독과 방출 대기·정리 코드를 읽기 쉽게 하려는 선택이었습니다.

### 설명 — 실제 사용과 경계

- 버전은 제출본과 조사 시점 main 모두 `turbine:1.2.1`이다. `core:testing`에서 `api`로 제공하지만 소비 모듈의 연결은 테스트 의존성이다. 앱 운영 경로에 쓰지 않는다.
- Presenter 테스트는 `presenterFlow(...).onEach { latest = it }.test { ... }`로 구독한다. `awaitItem()`으로 상태를 받고 `awaitItemMatching` helper는 조건에 맞을 때까지 중간 방출을 소비한다. UI 모델에 이벤트 람다가 있어 재구성마다 새 값이 나올 수 있으므로 정확한 방출 개수·모든 중간 상태 순서를 검증하는 방식은 아니다.
- 검색 실패는 `SearchContent.Error`나 `loadMoreError`, 쓰기 실패는 `userMessage` 같은 **방출된 오류 상태**를 검사한다. 조사한 과제 테스트는 `awaitError()`로 Flow 자체의 종료 예외를 검사하지 않았고, `awaitComplete()`도 호출하지 않았다. 두 API는 Turbine의 일반 기능과 과제의 실제 사용을 구분한다.
- 테스트 종료에는 `cancelAndIgnoreRemainingEvents()`를 사용한다. 남은 이벤트를 무시하므로 모든 방출을 검증했다는 뜻은 아니다. 늦은 검색 응답 혼입 검사는 `cancelAndConsumeRemainingEvents()`로 남은 Item을 확인해 이전 검색 결과가 섞이지 않았는지 검사한다.
- Room DAO 관찰·Soil Subscription의 Flow도 Turbine으로 검사한다. Molecule이 있어야만 Turbine을 사용할 수 있는 것은 아니다. 해당 Room Subscription 테스트의 `.test(timeout = ROOM_TIMEOUT)`은 30초로 설정되어 있다.

### 꼬리질문 — 둘을 함께 사용한 예

- 예시 하나를 설명해보세요. → SearchPresenter를 Molecule Flow로 실행하고 Turbine으로 Loading을 확인한다. Fake API의 CompletableDeferred로 자바 응답을 늦춘 채 코틀린 검색을 보내 코틀린 결과를 확인한다. 자바 응답을 나중에 풀고 남은 상태를 검사해 이전 검색 결과가 섞이지 않는지 확인한다.
- 일반 collect나 toList와 무엇이 다른가요? → 유한 Flow는 toList로도 충분하다. 계속 상태를 내보내는 Flow에서는 별도 수집 Job·저장 목록·이벤트 대기·취소를 직접 관리할 수 있는데, Turbine은 이를 테스트용 API로 정리한다. 필수 라이브러리라는 뜻은 아니다.
- delay를 없애면 모든 비동기 문제가 해결되나요? → 아니다. awaitItem은 실제 방출을 기다리고, fake gate·테스트 scheduler로 실행 순서를 제어한다. Soil 작업은 테스트 scheduler 밖에서 시작할 수 있어 요청 시작 Channel도 사용한다. 임의 delay가 불필요해지는 부분이 있지만 전체 경합을 자동 통제하지 않는다.
- timeout과 취소에서 주의할 점은요? → await 계열은 방출이 없으면 timeout으로 실패하지만 조건 helper는 중간 상태를 계속 건너뛸 수 있다. 필요한 경우 전체 시나리오의 제한도 검토해야 한다. 취소·남은 이벤트 무시는 의도한 관찰 종료인지 확인하고, 테스트 종료의 취소를 앱의 오류 처리로 혼동하지 않는다.
- 순서·완료·오류를 모두 검증했나요? → 필요한 상태 전이와 특정 늦은 응답 경계를 확인했다. 정확한 전체 방출 순서, 자연 완료, Flow 종료 예외를 모두 검사했다고 말하지 않는다.

### 근거·미확인

Q17과 같은 제출 커밋 `f9f6b2290199b354eb2cb79f998ef4147b063b17`, 조사 main `6f80ef0c568626bcdb08d6a81d5229e214805774`의 의존성·Presenter/Room 테스트를 읽었다. 빌드·테스트 재실행은 하지 않았다.

- [TurbineExtensions](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/core/testing/src/main/kotlin/io/github/easyhooon/booksearch/core/testing/TurbineExtensions.kt)
- [SearchPresenterTest](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/feature/search/src/test/kotlin/io/github/easyhooon/booksearch/feature/search/SearchPresenterTest.kt), [FavoriteSubscriptionKeysTest](https://github.com/easyhooon/book-search-android/blob/6f80ef0c568626bcdb08d6a81d5229e214805774/core/data/src/test/kotlin/io/github/easyhooon/booksearch/core/data/FavoriteSubscriptionKeysTest.kt)
- [Cash App 공식 Turbine README](https://github.com/cashapp/turbine): Flow 테스트용 수집·await·timeout·취소·미소비 이벤트 검사 기능을 설명한다.

Turbine의 일반 기능을 실제 사용한 기능으로 바꾸어 말하지 않는다. Molecule·Turbine을 함께 썼다는 사실만으로 UI·프로세스 복원이나 모든 경합을 검증했다고 주장하지 않는다.

## Q19. Hilt 대신 Metro를 선택한 이유와 성능상 장점은 무엇인가요?

### 30~45초 답변

Metro의 Kotlin 컴파일러 플러그인 방식과 명시적인 그래프 조립을 사용해보고 싶었습니다. DI용 KSP·kapt의 소스 생성 단계를 줄일 수 있고, 과제에서는 앱 그래프와 세 화면 그래프를 선언해 factory로 만들고 Navigation 3 엔트리에서 retain했습니다. 다만 Hilt도 컴파일 타임 DI이고 생성 코드를 실행하므로, Metro가 Hilt보다 앱 실행이 무조건 빠르다고 말할 수는 없습니다. 이 과제의 Hilt 비교 측정은 없으며, Metro 버전 때문에 빌드 실행 JDK 21이 필요해 원문의 JDK 17 조건을 충족하지 못한 비용도 있습니다.

### 목적·실제 활용·한계

| 목적/장점 | 실제 적용 | 한계 |
| --- | --- | --- |
| DI 빌드 단계 축소 | Metro 1.4.5 compiler plugin으로 graph/factory 구현 생성 | DI용 processor를 쓰지 않는다는 뜻. Room compiler는 core:database에서 KSP를 계속 사용한다 |
| 그래프·바인딩 명시 | AppGraph + 화면 GraphExtension 3개, @Provides/@Inject/@ContributesBinding/@ContributesTo | Hilt도 바인딩·그래프 검증을 제공한다. 검증 자체를 Metro만의 기능으로 설명하지 않는다 |
| 객체 공유 범위 | 앱의 Retrofit·OkHttp·Room·Soil·Coil은 AppScope, 화면 context는 각 ScreenScope의 SingleIn | scope는 인스턴스 재사용 범위다. 코루틴 종료·Nav3 pop 처리를 Metro가 자동 책임진다는 뜻은 아니다 |
| 화면 수명과 연결 | 생성된 factory로 graph를 만들고 엔트리에서 retain | 엔트리 수명은 retain decorator와 앱이 연결한다. 커스텀 KSP retain 함수 생성기는 없다 |
| 확장 기능 | 라이브러리는 KMP·함수 주입 등을 지원 | 과제는 Android 전용. Presenter 함수 직접 @Inject·private member injection·Activity AppComponentFactory 생성자 주입을 사용하지 않았다 |
| 도입 비용 | 기존 Hilt 사용 경험과 블로그 migration 경험을 바탕으로 선택 | Kotlin compiler 호환성과 JDK 21 요구, 낯선 그래프 패턴의 학습·유지 비용. 팀 도입 성과로 확대하지 않는다 |

### 꼬리질문 — 빌드와 런타임을 구분해서 설명하기

Q. KSP/kapt와 무엇이 다른가요?

kapt는 Kotlin에서 Java stub을 만들고 Java annotation processor를 실행한다. KSP는 Kotlin symbol을 읽어 코드를 생성한다. 생성 소스는 이후 컴파일에 참여한다. Metro는 Kotlin compiler의 FIR/IR에서 선언·그래프를 처리하고 코드를 생성하므로 DI용 별도 processor와 생성 소스 컴파일 경로를 피할 수 있다. “코드를 아예 생성하지 않는다”거나 “앱 전체가 한 번만 컴파일된다”는 의미는 아니다. Gradle task·증분 빌드·다른 processor 비용은 남는다. Hilt도 KSP를 지원하므로 Hilt를 반드시 kapt 방식으로만 비교하면 안 된다.

Q. 런타임에서 reflection이 없으니 Hilt보다 빠른가요?

Metro는 미리 연결된 provider/factory 생성 코드를 실행한다. Hilt의 기반인 Dagger도 생성 코드로 DI를 구현한다. 따라서 runtime discovery 회피가 Metro의 특성인 것은 맞지만, Hilt 대비 성능 우위를 자동으로 증명하지는 않는다. graph 생성·초기화 microbenchmark와 실제 앱 시작·렌더링·메모리 사용은 별개다.

Q. 블로그의 47%·56% 수치를 이 과제 성과로 말해도 되나요?

아니다. [제작자의 초기 소개](https://www.zacsweers.dev/introducing-metro/)는 약 35개 모듈의 CatchUp을 anvil-ksp + K2 kapt dagger-compiler에서 옮긴 사례다. 하위 모듈 ABI 변경 47%, non-ABI 변경 56% 개선을 보고했지만 Hilt를 사용한 이 과제의 전후 비교가 아니다. 본인의 [Metro 적용 글](https://velog.io/@mraz3068/Metro-Apply)도 직접 benchmark를 아직 하지 않았다고 명시한다.

[공식 성능 문서](https://zacsweers.github.io/metro/latest/performance/)의 2026-07-30 공개 결과는 결정적으로 생성한 다중 모듈 workload에서 Metro 1.4.0과 Dagger KSP/KAPT+Anvil 등을 비교한다. Gradle Profiler의 10회 측정 중앙값이며 clean build는 제외한다. 런타임 결과는 graph 생성·초기화 측정이다. 이 역시 Metro 1.4.5를 쓰는 본 과제의 Hilt 비교가 아니다. 수치보다 측정 대상·버전·환경·시나리오를 먼저 설명한다.

Q. Hilt에서는 원하는 수명을 만들 수 없나요?

Hilt도 custom component를 제공한다. Android 기본 컴포넌트·ViewModel 통합은 Hilt의 장점이다. 이번 선택은 Nav3 엔트리와 직접 연결하는 graph/factory 패턴을 사용해보려는 판단이며, Hilt로 불가능해서 택했다는 설명은 아니다.

Q. 블로그에서 얻은 실제 학습은 무엇인가요?

Metro migration 중 public provider가 DataStore Preferences 타입을 노출하면서 의존성을 implementation으로 숨겨, 소비 모듈에서 타입을 해석하지 못하는 문제를 재현 저장소와 Discussion으로 확인했다. 이 경험은 공개 API의 타입을 소비자의 compile classpath에 노출해야 한다는 모듈 계약을 이해한 사례다. implementation은 선언한 모듈의 compile classpath에서 빠지는 것이 아니라 소비 모듈에 전이 노출되지 않는 것이다. Hilt에서 모든 implementation 선언이 안전하다는 일반론으로 확대하지 않는다.

Q. 함수 주입은 그냥 파라미터 없이 호출하면 되나요?

[공식 주입 문서](https://zacsweers.github.io/metro/latest/injection-types/#top-level-function-injection)는 opt-in과 생성 bridge 타입·graph 접근을 설명한다. 블로그의 짧은 무인자 호출 예시는 전체 사용 계약으로 설명하기 부족하다. 이 과제는 해당 기능을 사용하지 않았으며 Root→Presenter 인자로 의존성을 전달한다.

### 근거·미확인

본인의 [Metro 찍먹해보기](https://velog.io/@mraz3068/Metro-Try-Out), [Metro 적용해보기](https://velog.io/@mraz3068/Metro-Apply) 본문 전체와 [Metro 공식 README](https://github.com/ZacSweers/metro), [Dagger 생성 코드 설명](https://dagger.dev/dev-guide/), [Dagger/Hilt KSP](https://dagger.dev/dev-guide/ksp.html), [kapt stub 처리](https://kotlinlang.org/docs/kapt.html), [Hilt custom components](https://dagger.dev/hilt/custom-components.html)를 대조했다. 블로그의 특정 시점 API·장점 소개를 현재 사용 사실로 섞지 않는다.

공개 main `510d7a601402c00a2caed55f602be59e2738d990`와 제출 `f9f6b2290199b354eb2cb79f998ef4147b063b17`의 Metro/Soil 버전과 graph/factory/retain 구성은 동일한 기준이다. Writer 제거에 따른 graph 의존성 차이는 Q8에 분리했다. 과제 source·제출 ZIP·APK를 바꾸거나 build 측정을 실행하지 않았다.

- [AppGraph](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/app/src/main/kotlin/io/github/easyhooon/booksearch/AppGraph.kt)
- [SearchScreenGraph](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchScreenGraph.kt)
- [엔트리에서 graph retain](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchScreenRoot.kt#L23)
- [Room KSP 설정](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/core/database/build.gradle.kts)
- [JDK 조건·미충족 기록](https://github.com/easyhooon/book-search-android/blob/510d7a601402c00a2caed55f602be59e2738d990/docs/SPEC.md#jdk-기준)

### 다른 라이브러리 질문을 추가한다면

현재 retain(Q5), Soil(Q6~8), Molecule(Q17), Turbine(Q18), Metro(Q19)가 있다. 다음 후보는 **Navigation 3의 백스택 소유권·contentKey·엔트리 제거와 retain 정리**다. Q4/Q5의 꼬리질문으로 먼저 연습하면 충분하며 별도 질문을 무조건 늘리지 않는다. Coil·Timber·Retrofit은 낯선 이름 소개보다 과제의 이미지 인증 분리·오류 로그·취소 계약을 설명할 때 다룬다.

## Q20. AI가 작성한 코드와 테스트가 같은 오류를 공유할 수도 있는데, 어떻게 검증했나요?

### 30~45초 답변

맞습니다. 구현을 그대로 따라 만든 테스트는 같은 오해를 공유할 수 있어서, 코드보다 기획서의 사용자 행동과 기대 결과를 기준으로 테스트 케이스를 정하려 했습니다. 예를 들어 느린 저장 뒤 해제를 누르면 마지막 의도가 DB에 남아야 한다는 계약입니다. 제출 후 Writer를 제거할 때는 저장을 누락하거나 화면 이탈 시 작업을 취소하고, 화면별 actor를 나누는 결함을 넣어 테스트가 실제로 실패하는지 확인했습니다. 복원 후 전체 검사도 통과했습니다. 다만 세 결함의 검출 근거이며 AI 테스트의 독립성이나 모든 동작의 정확성을 보장하는 것은 아닙니다.

### 설명 — 구현과 기대 결과의 근거를 분리하기

- **기획서 기반 테스트를 작성하려던 의도:** AI에 구현을 맡길수록 테스트가 중요하다고 판단했다. 요구 동작·사용자 시나리오에서 기대 결과를 먼저 정하려 했다는 본인 설명이다. 모든 테스트가 구현 전에 작성됐거나 별도의 사람이 독립 작성했다는 근거는 없다.
- **검사 대상:** 클래스 호출 횟수만이 아니라 저장→해제 순서의 최종 DB 상태, 화면 이탈 중 접수한 작업의 완료, 실제 Room 구독 결과 등 외부에서 확인할 수 있는 계약을 검증했다. 테스트별 fake DAO와 실제 메모리 Room의 범위는 구분한다.
- **검사가 실패할 수 있는지 확인:** 제출 후 개선 단계에서 세 운영 코드 결함을 하나씩 임시 적용했다. 관련 테스트 실패를 확인하고 원복한 뒤 최종 전체 검사를 실행했다. 결함 코드는 커밋하지 않았다.

| 임시로 깨뜨린 동작 | 기록에서 확인한 검출 결과 |
| --- | --- |
| DAO 저장 무시 | Mutation 경계 검사와 실제 Room 목록 구독 검사 실패 |
| pop에서 `job.complete()` 대신 `job.cancel()` | 진행 중·대기 명령과 화면 간 순서 관련 수명 테스트 4개 실패 |
| 화면별로 다른 Mutation ID 사용 | 느린 저장·빠른 해제의 최종 DB 상태가 저장으로 남아 실패. retain 재진입 검사도 실패 |

actor 분리 검사는 같은 지연시간만으로 충분하지 않아 작업 시간을 다르게 둔 최종 상태 사례를 포함했다. 이는 테스트의 자극 조건도 검토한 사례이며, 포괄적인 mutation testing 도구나 mutation score를 적용한 것은 아니다.

### 꼬리질문 — 독립성·실행 범위

- 기획서 기반이면 독립성이 보장되나요? → 아니다. 기획서 자체가 틀리거나 AI가 요구를 잘못 해석할 수도 있다. 구현을 기대값의 유일한 근거로 삼지 않으려는 접근이며, 시나리오·예외 조건·기대 결과를 사람이 검토해야 한다.
- 테스트도 AI가 작성했나요? → AI의 구현·테스트 작성과 실행을 포함한다. 본인이 모든 테스트를 직접 작성했거나 별도 독립 검증자가 작성했다고 말하지 않는다. 본인의 판단과 실제 검사 결과를 구분해 설명한다.
- 통과한 테스트 수만으로 충분하지 않나요? → 개수는 보장 범위가 아니다. 실제로 깨뜨린 동작이 관련 테스트에서 실패하는지를 함께 확인했다. 세 결함 외의 오류는 여전히 놓칠 수 있다.
- 단위 테스트를 넘어 무엇을 확인했나요? → 실제 Soil·retain 수명과 메모리 Room 연결을 사용한 검사가 있다. fake의 지연·실패·취소 검사를 실제 기기 장애나 상용 E2E 전체 검증으로 표현하지 않는다.
- 제출 전에 결함 주입까지 했나요? → 이 근거는 제출 후 Writer 제거 단계다. 제출본 `f9f6b22`의 검증 성과로 소급하지 않는다.
- 화면 pop 검증이 프로세스 종료도 보장하나요? → 아니다. actor 자체 취소와 일반 pop도 다르며, 프로세스 종료 중 미완료 쓰기의 완료는 보장하지 않는다.

### 근거·미확인

기획서 기반으로 테스트 케이스를 정하려던 의도와 AI에 구현을 맡길수록 테스트가 중요하다는 판단은 본인의 추가 설명이다. 실제 결함 주입·원복·최종 검사 결과는 제출 후 [PR #2 검증 코멘트](https://github.com/easyhooon/book-search-android/pull/2#issuecomment-6107392839)와 [Writer 제거 검증 문서](https://github.com/easyhooon/book-search-android/blob/2722737d6648f9071cd80bb48749e0ceb864b38d/docs/WRITER_REMOVAL.md)의 기록에 근거한다.

해당 기록은 기준 140개→최종 145개 테스트, 실패·오류·skip 0, APK 빌드·lint 통과(오류0·경고2)를 보고한다. 이번 노트 작업은 기록을 읽은 것이며 검사를 다시 실행하지 않았다. 제출 후 단계에서는 실기기 재검증·프로세스 종료 QA·제출 패키지 재생성을 실행하지 않았다. 전체 요구의 완전한 무결성, 독립 작성된 테스트, 상용 E2E 전체 구현 또는 포괄적인 결함 검출률은 확인하지 않았다.

## Q21. `rememberUpdatedState`는 왜 사용했고, 효과의 키와 무엇이 다른가요?

### 30초 답변

효과의 키는 **언제 작업을 취소하고 다시 시작할지** 정하고, `rememberUpdatedState`는 **작업을 유지하면서 바뀐 값을 읽게** 합니다. 과제의 검색·즐겨찾기·상세 화면은 `LaunchedEffect(userMessage)`에서 스낵바를 띄운 뒤 `UserMessageShown`을 보냅니다. `showSnackbar`로 기다리는 동안 재구성이 일어나더라도, 효과를 다시 시작하지 않고 최신 `eventSink`를 호출하려고 `rememberUpdatedState(uiState.eventSink)`를 사용했습니다. 검색의 `LoadMoreEffect`도 `gridState, itemCount`를 재시작 키로 두고, 스크롤을 관찰하는 동안 `onLoadMore`는 최신 참조로 읽습니다.

### 꼬리질문

- **왜 콜백을 키에 넣지 않나요?** 콜백이 바뀔 때마다 스낵바 표시나 스크롤 수집을 취소·재시작할 필요는 없기 때문입니다. 반대로 그 변경이 작업을 다시 시작해야 하는 의미라면 키에 넣어야 합니다.
- **그냥 `remember`하면 안 되나요?** `remember`는 값을 보관하고 `remember(key)`는 키가 바뀌면 다시 계산하지만, 이미 실행 중인 효과가 붙잡은 콜백을 자동으로 최신화하지는 않습니다. suspend 이후 오래된 콜백을 호출할 가능성을 구분해야 합니다.
- **다른 효과와는 어떻게 구분하나요?** `LaunchedEffect`는 키에 묶인 코루틴 작업, `DisposableEffect`는 등록과 해제, `SideEffect`는 성공한 재구성 뒤 외부 객체 갱신, `produceState`는 코루틴 결과를 Compose `State`로 내보낼 때 씁니다. Reed의 로딩 지연 예시는 `produceState(false, delayMillis)`에서 기본 500ms를 기다린 뒤 상태를 바꾸는 형태로, 최신 콜백 참조를 유지하는 문제와는 다릅니다.

### 근거·미확인

[검색 화면과 `LoadMoreEffect`](https://github.com/easyhooon/book-search-android/blob/7e0479d0f1bf77f80378c40762637027615437a8/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchScreen.kt), [즐겨찾기 화면](https://github.com/easyhooon/book-search-android/blob/7e0479d0f1bf77f80378c40762637027615437a8/feature/favorites/src/main/kotlin/io/github/easyhooon/booksearch/feature/favorites/FavoritesScreen.kt), [상세 화면](https://github.com/easyhooon/book-search-android/blob/7e0479d0f1bf77f80378c40762637027615437a8/feature/detail/src/main/kotlin/io/github/easyhooon/booksearch/feature/detail/BookDetailScreen.kt)과 [Android 공식 부수 효과 설명](https://developer.android.com/develop/ui/compose/side-effects)을 대조했다. 콜백이 실제로 매번 바뀌거나, 이 래퍼가 관찰된 버그를 고쳤다고 단정하지 않는다. 콜백이 이미 안정적으로 유지된다면 필요한 방어는 아닐 수 있다. Reed 사례는 사용자 제공 설명이며 해당 소스는 이번에 확인하지 않았다.

## Q22. `rememberSerializable`이 있으면 `rememberSaveable`은 필요 없지 않나요?

### 30초 답변

`rememberSerializable`은 Bundle 타입 제한 없이 `@Serializable` 모델을 그대로 저장할 수 있어 편하지만, 상위호환이라고 보지는 않습니다. 저장 위치는 둘 다 saved instance state이므로 크기 제한과 "최소 상태만 저장" 원칙은 같습니다. 그래서 과제에서도 함께 썼습니다. Presenter의 검색어·정렬처럼 여러 필드를 묶은 저장 상태는 `@Serializable` data class와 `rememberSerializable`로 두었고, Screen의 Boolean·String이나 `LazyGridState`처럼 Compose가 `Saver`를 이미 제공하는 상태는 `rememberSaveable`을 그대로 썼습니다.

### 설명 — 선택 기준

| 기준 | `rememberSaveable` | `rememberSerializable` |
| --- | --- | --- |
| 저장 계약 | Bundle에 넣을 수 있는 타입(원시 타입·String·Parcelable 등) + `Saver` | `KSerializer`가 있는 타입. reified 오버로드는 serializer를 자동으로 찾고, 명시적 `serializer`/`stateSerializer`도 받는다 |
| 잘 맞는 경우 | 원시 값, `LazyListState.Saver`·`LazyGridState.Saver` 등 기존 Saver가 있는 Compose 상태 holder, 이미 Parcelable인 타입 | 여러 필드를 묶은 저장용 data class, NavKey처럼 이미 `@Serializable`인 모델 재사용, Parcelable 없이 공통 코드에서 쓰는 KMP 상태 |
| 비용 | 비원시 타입마다 `Saver`(`listSaver`/`mapSaver`) 작성 | serialization 플러그인·의존성, 비교적 최신 `runtime-saveable` 버전 요구. Saver만 있는 상태 holder에는 직접 KSerializer를 만들어야 한다 |
| 공통 한계 | Bundle 크기 제한(`TransactionTooLargeException`), 큰 목록·객체 저장 금지 | 동일. 타입 제한이 풀리는 것이지 크기 제한이 풀리는 것은 아니다 |

- "모든 타입"이 아니라 **직렬화 가능한 모든 타입**이다. 직렬화할 수 없는 상태(콜백, 코루틴, 리소스 핸들)는 저장 대상이 아니며 retain이나 재생성 쪽 문제다.
- 저장 형태를 직접 줄이는 일은 둘 다 할 수 있다. Saver로는 ID만 저장하고, KSerializer로도 필요한 필드만 인코딩할 수 있다. 어느 API를 쓰느냐보다 무엇을 저장하느냐가 핵심이다.
- `inputs`가 바뀌면 상태를 다시 초기화하는 동작은 같다. 복원 때 저장된 값이 inputs와 일치하는지 검증하지 않는 점도 같다.

### 꼬리질문

- 그럼 앞으로 전부 `rememberSerializable`로 바꾸면 되지 않나요? → 모델이 이미 `@Serializable`이면 그렇게 하는 게 자연스럽다. 하지만 `LazyGridState`처럼 Saver만 제공되는 상태 holder까지 KSerializer를 새로 만들면 득보다 비용이 크다. 일관성 하나만을 위해 바꾸지는 않는다.
- Bundle 제한이 없다면 검색 결과 목록도 저장해도 되나요? → 아니다. 결과는 Soil 캐시·네트워크로 다시 얻고, 저장 상태에는 검색어·정렬 같은 조건만 둔다(Q4, Q6).
- `retain`과는 어떻게 다른가요? → retain은 직렬화 없이 객체 인스턴스를 유지하지만 프로세스 종료를 견디지 못한다. 저장 API는 직렬화된 최소 값을 프로세스 재생성 뒤에도 복원한다(Q5).
- Java `Serializable`과 같은 건가요? → 아니다. kotlinx.serialization의 `@Serializable`/`KSerializer`이며, 리플렉션 기반 Java 직렬화와 다르다.

### 근거·미확인

공식 [rememberSerializable 레퍼런스](https://developer.android.com/reference/kotlin/androidx/compose/runtime/saveable/rememberSerializable.composable): 값 오버로드(`serializer`), `MutableState` 오버로드(`stateSerializer`), `configuration`(`SavedStateConfiguration`) 파라미터, saved instance state를 통한 저장을 확인했다. [MutableStateSerializer 패키지](https://developer.android.com/reference/kotlin/androidx/savedstate/compose/serialization/serializers/package-summary)와 [상태 저장 가이드](https://developer.android.com/develop/ui/compose/state-saving)의 Bundle 크기 제한 설명도 대조했다. 최소 지원 버전은 오버로드마다 다를 수 있어 정확한 버전을 숫자로 단정하지 않는다.

과제 main `106d98d4084b8e2365a33cadd071f62aa3f998b8` 기준:

- [SearchPresenter — `@Serializable SearchSavedState` + `rememberSerializable`](https://github.com/easyhooon/book-search-android/blob/106d98d4084b8e2365a33cadd071f62aa3f998b8/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchPresenter.kt#L70)
- [SearchScreen — `rememberSaveable(..., saver = LazyGridState.Saver)`](https://github.com/easyhooon/book-search-android/blob/106d98d4084b8e2365a33cadd071f62aa3f998b8/feature/search/src/main/kotlin/io/github/easyhooon/booksearch/feature/search/SearchScreen.kt#L117)
- [FavoritesScreen — Boolean `rememberSaveable`](https://github.com/easyhooon/book-search-android/blob/106d98d4084b8e2365a33cadd071f62aa3f998b8/feature/favorites/src/main/kotlin/io/github/easyhooon/booksearch/feature/favorites/FavoritesScreen.kt#L56)

코드 검색만 했고 빌드·프로세스 종료 복원 테스트를 다시 실행하지 않았다. 두 API의 인코딩 성능 차이는 측정하지 않았다.
