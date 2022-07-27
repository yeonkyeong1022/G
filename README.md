### 요구사항 분석

1. 목록 화면 :
    - 전체목록을 페이징 처리해 조회
    - 제목/내용/작성자 항목으로 검색과 페이징 처리 가능
2. 등록 화면 
    - 새로운 글을 등록
    - 처리 후 다시 목록화면으로 이동
3. 조회 화면 
    - 목록화면에서 특정한 글을 선택하면 자동으로 조회화면으로 이동
    - 수정/삭제가 가능한 화면으로 버튼을 클릭해서 이동할 수 있음
4. 수정/삭제 화면 
    - 수정화면에서 삭제가 가능
    - 삭제 후에는 목록페이지로 이동
    - 글을 수정하는 경우에는 다시 조회화면으로 이동해서 수정된 내용 확인

### API 규격서

| 기능 | URL | GET/POST | 기능 | Redirect URL |
| --- | --- | --- | --- | --- |
| 목록 | /guestbook/list | GET | 목록/페이징/검색 |  |
| 등록 | /guestbook/register | GET | 입력 화면 |  |
| 등록 | /guestbook/register | POST | 등록 처리 | /guestbook/list |
| 조회 | /guestbook/erad | GET | 조회 화면 |  |
| 수정 | /guestbook/modify | GET | 수정/삭제 기능 화면 |  |
| 수정 | /guestbook/modify | POST | 수정 처리 | /guestbook/read |
| 삭제 | /guestbook/remove | POST | 삭제 처리 | /guestbook/list |

### 엔티티 관계도
![image](https://user-images.githubusercontent.com/89283563/181215114-2ead3624-9c65-4a84-b2b8-c2de8633e132.png)



### 프로젝트 디자인
![image](https://user-images.githubusercontent.com/89283563/181114182-36a1a907-acdf-4c6c-bcbe-51af789714d0.png)
![image](https://user-images.githubusercontent.com/89283563/181114359-e601112f-d106-44ed-ad4d-007855723996.png)
![image](https://user-images.githubusercontent.com/89283563/181114411-465da768-9a45-4bbf-9f78-21b622805170.png)


