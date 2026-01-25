---
title: render에 한글설치하는 방법
categories: [dev]
comments: true
---

render.io 에 프로젝트를 배포하다가 entrypoint 파일에 한글을 추가해야
로그나 주석의 한글을 알아먹을 수 있단 사실을 깨달았다. 어떻게 하냐면

```
# =========================
# 🔤 UTF-8 로케일 강제 (한글 로그 깨짐 방지)
# =========================
export LANG=C.UTF-8
export LC_ALL=C.UTF-8
export JAVA_TOOL_OPTIONS="-Dfile.encoding=UTF-8"

echo "[entrypoint] LANG=${LANG}, LC_ALL=${LC_ALL}"
```

이걸 추가해주면 된다.

헤헷>,<
