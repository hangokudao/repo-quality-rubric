# Repo Quality Rubric

[English](README.md)

저장소 품질을 근거 중심으로 검토하는 Codex 스킬입니다.

이 스킬은 저장소, CLI, 패키지, 프론트엔드 앱, 문서 세트, 공개 릴리스, AI-agent workflow를 검토한 뒤 **가중치가 적용된 100점 기준 점수와 구체적인 근거**를 남기도록 돕습니다.

이 스킬로 Codex가 하는 일은 간단합니다.

- 프로젝트 유형을 먼저 분류하기
- 유형에 맞는 가중치 기준 고르기
- 파일, 테스트, 빌드, 패키지 결과 같은 실제 증거 확인하기
- 반드시 고칠 문제와 개선하면 좋은 문제를 분리하기
- 확인하지 못한 영역을 따로 적기

## 결과물 예시

```md
# Repo Quality Review

Total Score: 86/100

## Score Breakdown

| Criterion | Weight | Score | Evidence |
|---|---:|---:|---|
| User-facing quality | 20 | 16 | Generated examples are clear, but one README link is stale |

## Must Fix

1. ...

## Not Verified

- ...
```

## 스킬 위치

설치 대상 스킬은 여기에 있습니다.

```text
skills/repo-quality-rubric/
```

## 포함된 기준

- 기본 저장소 준비도
- 코드 리뷰 품질
- CLI/패키지 릴리스 품질
- 공개 저장소 준비도
- 프론트엔드/제품 디자인 리뷰
- 접근성
- 보안
- AI-agent workflow 평가

## 사용법

Codex에 스킬을 설치하거나 복사한 뒤 이렇게 호출하면 됩니다.

```text
Use $repo-quality-rubric to review this repository and report a weighted 100-point score with evidence.
```

자연어로 이렇게 말해도 됩니다.

```text
이 저장소를 공개해도 될지 점검해줘. 항목별로 몇 점인지, 왜 그 점수인지 근거까지 보여줘.
```

## 참고

- 이 저장소는 Codex 스킬을 담고 있으며, 정식 Codex 플러그인은 아닙니다.
- 검토 중 `AGENTS.md`나 프로젝트 규칙 파일을 자동으로 수정하지 않도록 설계했습니다.
- MIT 라이선스를 사용합니다.
