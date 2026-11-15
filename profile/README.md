<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/CluVi-prometheus/.github/main/profile/assets/banner-dark.svg">
  <img alt="CluVi — Multimodal VQA · Agent for CS counselors" src="https://raw.githubusercontent.com/CluVi-prometheus/.github/main/profile/assets/banner-light.svg" width="100%">
</picture>

<div align="center">

### 사진 민원을 읽고 CS 상담원을 돕는 멀티모달 VQA · 에이전트

고객이 올린 리뷰 글과 사진에서 **무슨 결함인지 · 어느 부위인지 · 사진 어디에 보이는지**를 분석 카드로 만들고,<br />
상담원이 물으면 에이전트가 그 카드와 주문 · 정책 조회를 근거로 답합니다.

![Qwen2.5-VL-7B](https://img.shields.io/badge/Qwen2.5--VL--7B-1f3d34?style=flat-square)
![PyTorch](https://img.shields.io/badge/PyTorch-1f3d34?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-1f3d34?style=flat-square&logo=huggingface&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-1f3d34?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-1f3d34?style=flat-square&logo=react&logoColor=white)

**[메인 레포 `cluvi` 바로 가기 →](https://github.com/CluVi-prometheus/cluvi)**

</div>

<br />

## 흐름

```mermaid
flowchart LR
    A[리뷰 글 + 사진] --> B[VLM 분석<br/>Qwen2.5-VL-7B]
    B --> C[(분석 카드)]
    Q[상담원 질문] --> D[에이전트]
    C --> D
    T[주문 · 정책 도구] --> D
    D --> R[답변 + 근거]
```

연구 목표는 정확도를 지키면서 VLM 추론 비용(시각 토큰 · 지연 · 메모리)을 줄이는 것입니다.

## 레포

| 레포 | 하는 일 |
|---|---|
| **[cluvi](https://github.com/CluVi-prometheus/cluvi)** | 메인 레포. 팀이 맞춘 것 · 결과 비교 · 서비스 · 상담원 화면 |
| [jimni3155](https://github.com/CluVi-prometheus/jimni3155) | 개인 실험 레포 |
| [joungjubinn](https://github.com/CluVi-prometheus/joungjubinn) | 개인 실험 레포 |
| [vmgfh878-art](https://github.com/CluVi-prometheus/vmgfh878-art) | 개인 실험 레포 · Heavy 경로 (제로샷 · HAWK · LoRA) |

## 일정

베이스라인 `10/27–11/13` → 토큰 선택 실험 `~12/8` → 에이전트 · API `~1/8` → 데모 통합 · 평가 `~1/22` → 최종 제출 `1/30`

진행 상황은 [마일스톤](https://github.com/CluVi-prometheus/cluvi/milestones)에서 봅니다.

## 팀

<table>
  <tr>
    <td align="center"><a href="https://github.com/jimni3155"><img src="https://github.com/jimni3155.png?size=120" width="64" alt="jimni3155" /><br /><sub><b>jimni3155</b></sub></a></td>
    <td align="center"><a href="https://github.com/joungjubinn"><img src="https://github.com/joungjubinn.png?size=120" width="64" alt="joungjubinn" /><br /><sub><b>joungjubinn</b></sub></a></td>
    <td align="center"><a href="https://github.com/vmgfh878-art"><img src="https://github.com/vmgfh878-art.png?size=120" width="64" alt="vmgfh878-art" /><br /><sub><b>vmgfh878-art</b></sub></a></td>
  </tr>
</table>

<sub>프로메테우스 6팀 · 2026 &nbsp;|&nbsp; 데이터셋에는 고객 사진이 들어 있어 공개하지 않습니다.</sub>
