# :: 과제#1 - Todo List & API

# 1-1) 사전과제 진행 가이드

- REST API 통신은 'axios' 라이브러리를 사용해주세요.
- Design Library(eg. Ant Design, Material UI, Chakra UI...)를 사용하셔도 됩니다.
- UI Mockup은 참고용이니 동일하게 구현하셔도 되고 다르게 구현하셔도 됩니다.
- 구현 사항을 꼼꼼하게 읽어 보신 후 과제를 진행해주세요.

# 1-2) 클라이언트 구현 과제 안내

## Assignment - Todo List

- Todo List API를 호출하여 Todo List CRUD 기능을 구현해주세요
  - [ ] 목록 / 상세 영역으로 나누어 구현해주세요
  - [ ] Todo 목록을 볼 수 있습니다.
  - [ ] Todo 추가 버튼을 클릭하면 할 일이 추가 됩니다.
  - [ ] Todo 수정 버튼을 클릭하면 수정 모드를 활성화하고, 수정 내용을 제출하거나 취소할 수 있습니다.
  - [ ] Todo 삭제 버튼을 클릭하면 해당 Todo를 삭제할 수 있습니다.
- ~~한 화면 내에서 Todo List와 개별 Todo의 상세를 확인할 수 있도록 해주세요.~~
  - [ ] 새로고침을 했을 때 현재 상태가 유지되어야 합니다.
  - [ ] ~~개별 Todo를 조회 순서에 따라 페이지 뒤로가기를 통하여 조회할 수 있도록 해주세요.~~
- ~~한 페이지 내에서 새로고침 없이 데이터가 정합성을 갖추도록 구현해주세요~~

  - [ ] 수정되는 Todo의 내용이 목록에서도 실시간으로 반영되어야 합니다

  
## 과제 참고 사항

1. 로컬 서버를 실행했을 때 생성되는 `db/db.json`이 DB 역할을 하게 됩니다. 해당 파일을 삭제하면 DB는 초기화 됩니다.

# 2-1) API 실행

```bash
> yarn

> yarn start # http://localhost:8080
```

# 2-2) API 스펙

## [Todos](#todos)

- [getTodos](#gettodos)
- [getTodoById](#getTodbyid)
- [createTodo](#createtodo)
- [updateTodo](#updatetodo)
- [deleteTodo](#deletetodo)

# <span id="todos">1-3) Todos</span>

## getTodos

### URL

- GET `/todos`

### 응답 예시

```json
{
  "data": [
    {
      "title": "hi",
      "content": "hello",
      "id": "z3FGrcRL55qDCFnP4KRtn",
      "createdAt": "2022-07-24T14:15:55.537Z",
      "updatedAt": "2022-07-24T14:15:55.537Z"
    },
    {
      "title": "hi",
      "content": "hello",
      "id": "z3FGrcRL55qDCFnP4KRtn",
      "createdAt": "2022-07-24T14:15:55.537Z",
      "updatedAt": "2022-07-24T14:15:55.537Z"
    }
  ]
}
```

## getTodoById

### URL

- GET `/todos/:id`

### 응답 예시

```json
{
  "data": {
    "title": "hi",
    "content": "hello",
    "id": "z3FGrcRL55qDCFnP4KRtn",
    "createdAt": "2022-07-24T14:15:55.537Z",
    "updatedAt": "2022-07-24T14:15:55.537Z"
  }
}
```

## createTodo

### URL

- POST `/todos`
- Parameter
  - title: string
  - content: string

### 응답 예시

```json
{
  "data": {
    "title": "hi",
    "content": "hello",
    "id": "z3FGrcRL55qDCFnP4KRtn",
    "createdAt": "2022-07-24T14:15:55.537Z",
    "updatedAt": "2022-07-24T14:15:55.537Z"
  }
}
```

## updateTodo

### URL

- PUT `/todos/:id`
- Parameter
  - title: string
  - content: string

### 응답 예시

```json
{
  "data": {
    "title": "제목 변경",
    "content": "내용 변경",
    "id": "RMfi3XyOKoI5zd0A_bsPL",
    "createdAt": "2022-07-24T14:25:48.627Z",
    "updatedAt": "2022-07-24T14:25:48.627Z"
  }
}
```

## deleteTodo

### URL

- DELETE `/todos/:id`

### 응답 예시

```json
{
  "data": null
}
```
