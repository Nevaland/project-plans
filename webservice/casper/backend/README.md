# Backend

## API 설계

### Board

- categories  
  id, name, (permission?)
  - GET /board/categories : 카테고리 목록
  - POST /board/categories : 카테고리 생성
- posts  
  id, author[user], created_date, viewer_num, categoriy[categories], title, content
  - GET /board/posts : 게시글 목록
  - POST /board/posts : 게시글 작성
  - PUT /board/posts/{post_id} : 게시글 수정
  - DELETE /board/posts/{post_id} : 게시글 삭제
- suggestions  
  id, author[user], created_date, type, title, content, chats{author[user], created_date, conetnt}
  - GET /board/suggestions : 제안 목록
  - POST /board/suggestions : 제안 작성
  - PUT /board/suggestions/{sugestions_id} : 제안 수정
  - DELETE /board/suggestions/{sugestions_id} : 제안 삭제
  - POST /board/suggestions/{sugestions_id}/chat : 제안 채팅 작성
- questsions // S.O.S  
  id, author[user], created_date, empired_date, category, status, title, content
  - GET /board/sos : 질문 목록
  - POST /board/sos : 질문 작성
  - PUT /board/sos/{sos_id} : 질문 수정
  - DELETE /board/sos/{sos_id} : 질문 삭제
- answers  
  id, author[user], created_date, question[questions], title, content
  - GET /board/answers : 답변 목록
  - POST /board/answers : 답변 작성
  - PUT /board/answers/{answers_id} : 답변 수정
  - DELETE /board/answers/{answers_id} : 답변 삭제

### User

- account  
  id, registrated_date, name, nickname, email, class, birth_date, photo, stacks, appeal[apeals], homepage, blog, contact, descryption, feed_mail  
  ...
- apeals  
  id, auther[user], updated_date, content
  - GET /board/apeals : 어필 목록
  - POST /board/apeals : 어필 작성 및 수정
  - DELETE /board/apeals : 어필 삭제
- activitists  
  id, user_id[user], visible, point, total_point
  - GET /board/activitists : 활동가 목록
  - POST /board/activitists : 활동가 등록
  - PUT /board/activitists : 활동가 정보 수정
- observers  
  id, user_id[user], visible, point, total_point
  - GET /board/activitists : 관측자 목록
  - POST /board/activitists : 관측자 등록
  - PUT /board/activitists : 관측자 정보 수정
- rescuers  
  id, user_id[user], visible, point, total_point
  - GET /board/activitists : 구조자 목록
  - POST /board/activitists : 구조자 등록
  - PUT /board/activitists : 구조자 정보 수정

### Activity

id, type(study, project, ctf), status(before, being, finished), author[user], title, content, participants{[user]}

- GET /board/activities : 활동 목록
- POST /board/activities : 활동 작성
- PUT /board/activities/{activity_id} : 활동 수정
- DELETE /board/activities/{activity_id} : 활동 삭제

### Log

- Ranking  
  year, [activist, observer, rescuer]{first_user, second_user, third_user, first_point, second_point, third_point}
  - GET /rankings : 랭킹 기록
  - POST /rankings : 랭킹 기록 작성
  - PUT /rangkins/{ranking_year} : 랭킹 기록 수정
- Point
- User
- Activity
- Post
- Connection

...
