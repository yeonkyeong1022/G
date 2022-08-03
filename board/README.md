
# Board Project

## 요구사항 분석

- 등록된 게시물은 보드 번호와 제목, 댓글 개수, 작성자, 작성일자를 가진다
- 등록된 사용자만 게시물 등록, 수정, 삭제할 수 있도록 한다.
- 등록된 사용자만 댓글 등록, 수정, 삭제할 수 있도록 한다
- 제목, 내용, 작성자 키워드를 이용해 게시물을 검색할 수 있도록 한다.

### API 규격서

- 보드
    
    
    | 방식 | 호출대상 | 파라미터 | 작업 |
    | --- | --- | --- | --- |
    | GET | /board/list | PageRequestDTO pageRequestDTO, Model model | 게시물 목록 출력 |
    | GET | /board/register | NULL | 게시물 등록 페이지 출력 |
    | POST | /board/register | BoardDTO dto, RedirectAttributes redirectAttributes | 게시물 생성 |
    | GET | /board/read | PageRequestDTO pageRequestDTO, Long bno, Model model | 게시물 조회 |
    | POST | /board/remove | long bno, RedirectAttributes redirectAttributes | 게시물 삭제 |
    | POST | /board/modify | BoardDTO dto, PageRequestDTO requestDTO, RedirectAttributes redirectAttributes | 게시물 수정 페이지 출력 |
    | GET | /board/modify | PageRequestDTO pageRequestDTO, Long bno, Model model | 게시물 수정 |

- 댓글
    
    
    | 방식 | 호출대상 | 파라미터 | 작업 |
    | --- | --- | --- | --- |
    | GET | /replies/board/{bno}(게시물 번호) | 게시물 번호 | 해당 게시물의 댓글 조회 |
    | POST | /replies/ | JSON으로 구성된 댓글 데이터 | 댓글 추가 |
    | DELETE | /replies/{rno} | 댓글 번호 | 댓글 삭제 |
    | PUT | /replies/{rno} | 댓글 번호+수정할 내용 | 댓글 수정 |

## 엔티티 관계도


## 프로젝트 디자인

- 댓글 목록 출력
<img width="1372" alt="화면 캡처 2022-08-03 224741" src="https://user-images.githubusercontent.com/89283563/182627419-c0b1909c-e041-4f5f-a6b0-518c559dc4a9.png">


- 게시글 조회 화면
<img width="1128" alt="화면 캡처 2022-08-03 224806" src="https://user-images.githubusercontent.com/89283563/182627436-97b606c9-31af-4a7c-a5bf-7dfd5393e370.png">


- 댓글 등록 화면
<img width="1282" alt="화면 캡처 2022-08-03 224849" src="https://user-images.githubusercontent.com/89283563/182627478-e3ec8916-c67f-4f92-bf0e-0ef519fca259.png">

