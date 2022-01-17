# Wechaty Authing 集成 POC

## CONTRIBUTING

Fork this repo.

Set env:

```bash
export AUTHING_USER_POOL_ID="xxx"
export AUTHING_USER_POOL_SECRET="xxx"
export PADLOCAL_TOKEN="xxx"
```

Start up:

```bash
npm start
```

## 以微信群作为上游数据源

修改 `src/index.ts`：

```ts
import './upstream';
// import './downstream';
```

[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggTFJcbiAgICBTdGFydDEoU3RhcnQpIFxuICAgIC0tQm90IOWQr-WKqC0tPiBjaGVjazFb5qOA5p-l576k5YaF55qE6Z2eIEF1dGhpbmcg55So5oi3XVxuICAgIC0tPiBhZGRVc2VyW-a3u-WKoCBBdXRoaW5nIOeUqOaIt-W5tua2iOaBr-aPkOmGkue7keWumuaJi-acuuWPt11cbiAgICAtLT4gRW5kMShFbmQpIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQifSwidXBkYXRlRWRpdG9yIjpmYWxzZSwiYXV0b1N5bmMiOnRydWUsInVwZGF0ZURpYWdyYW0iOmZhbHNlfQ)](https://mermaid.live/edit#eyJjb2RlIjoiZ3JhcGggTFJcbiAgICBTdGFydDEoU3RhcnQpIFxuICAgIC0tQm90IOWQr-WKqC0tPiBjaGVjazFb5qOA5p-l576k5YaF55qE6Z2eIEF1dGhpbmcg55So5oi3XVxuICAgIC0tPiBhZGRVc2VyW-a3u-WKoCBBdXRoaW5nIOeUqOaIt-W5tua2iOaBr-aPkOmGkue7keWumuaJi-acuuWPt11cbiAgICAtLT4gRW5kMShFbmQpIiwibWVybWFpZCI6IntcbiAgXCJ0aGVtZVwiOiBcImRlZmF1bHRcIlxufSIsInVwZGF0ZUVkaXRvciI6ZmFsc2UsImF1dG9TeW5jIjp0cnVlLCJ1cGRhdGVEaWFncmFtIjpmYWxzZX0)

[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggVERcbiAgICBTdGFydDEoU3RhcnQpIFxuICAgIC0tPiBhZGQxW-euoeeQhuWRmOS6uuS4uua3u-WKoOe-pOaIkOWRmF1cbiAgICAtLeeuoeeQhiBCb3Qg5L6m5ZCs5YWl576k5LqL5Lu2LS0-IGFkZDJbQm90IOWQkSBBdXRoaW5nIOazqOWGjOeUqOaIt11cbiAgICAtLeeUqOaIt-aPkOWPiiBCb3Qg5Y-R6YCB5omL5py65Y-3IC0tPiBhZGQzW0JvdCDlkJEgQXV0aGluZyDmm7TmlrDnu5HlrprnlKjmiLfmiYvmnLrlj7ddIFxuICAgIC0tPiBFbmQxKEVuZClcblxuICAgIFN0YXJ0MihTdGFydCkgXG4gICAgLS0-IGRlbDFb566h55CG5ZGY5Lq65Li65Yig6Zmk576k5oiQ5ZGYXVxuICAgIC0t566h55CGIEJvdCDkvqblkKzpgIDnvqTkuovku7YtLT4gIGRlbDJbQm90IOWQkSBBdXRoaW5nIOWIoOmZpOeUqOaIt11cbiAgICAtLT4gRW5kMihFbmQpIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQifSwidXBkYXRlRWRpdG9yIjpmYWxzZSwiYXV0b1N5bmMiOnRydWUsInVwZGF0ZURpYWdyYW0iOmZhbHNlfQ)](https://mermaid.live/edit#eyJjb2RlIjoiZ3JhcGggVERcbiAgICBTdGFydDEoU3RhcnQpIFxuICAgIC0tPiBhZGQxW-euoeeQhuWRmOS6uuS4uua3u-WKoOe-pOaIkOWRmF1cbiAgICAtLeeuoeeQhiBCb3Qg5L6m5ZCs5YWl576k5LqL5Lu2LS0-IGFkZDJbQm90IOWQkSBBdXRoaW5nIOazqOWGjOeUqOaIt11cbiAgICAtLeeUqOaIt-aPkOWPiiBCb3Qg5Y-R6YCB5omL5py65Y-3IC0tPiBhZGQzW0JvdCDlkJEgQXV0aGluZyDmm7TmlrDnu5HlrprnlKjmiLfmiYvmnLrlj7ddIFxuICAgIC0tPiBFbmQxKEVuZClcblxuICAgIFN0YXJ0MihTdGFydCkgXG4gICAgLS0-IGRlbDFb566h55CG5ZGY5Lq65Li65Yig6Zmk576k5oiQ5ZGYXVxuICAgIC0t566h55CGIEJvdCDkvqblkKzpgIDnvqTkuovku7YtLT4gIGRlbDJbQm90IOWQkSBBdXRoaW5nIOWIoOmZpOeUqOaIt11cbiAgICAtLT4gRW5kMihFbmQpIiwibWVybWFpZCI6IntcbiAgXCJ0aGVtZVwiOiBcImRlZmF1bHRcIlxufSIsInVwZGF0ZUVkaXRvciI6ZmFsc2UsImF1dG9TeW5jIjp0cnVlLCJ1cGRhdGVEaWFncmFtIjpmYWxzZX0)

## 以 Authing 作为上游数据源
