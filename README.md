<p align="center">
  <img src="https://raw.githubusercontent.com/softbank-hackathon-2026/.github/main/assets/banner.png" alt="Team Freesia · PieckPick — SoftBank Hackathon 2026 in Korea" width="100%">
</p>

<h1 align="center">PieckPick</h1>
<p align="center"><strong>인프라 담당자는 환경을 준비하고, 개발자는 앱 배포에 집중합니다.</strong></p>
<p align="center">저장소와 배포 환경을 선택하면 AI가 실행 구성을 추천하고,<br>배포 과정과 결과를 한곳에서 확인하는 배포 관리 플랫폼입니다.</p>

<p align="center">
  <img src="https://img.shields.io/badge/SoftBank_Hackathon_2026-Korea-blue" alt="SoftBank Hackathon 2026">
  <img src="https://img.shields.io/badge/React-TypeScript-61DAFB?logo=react&logoColor=white" alt="React">
  <img src="https://img.shields.io/badge/FastAPI-Python-009688?logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Terraform-AWS-7B42BC?logo=terraform&logoColor=white" alt="Terraform">
  <img src="https://img.shields.io/badge/GitHub_Actions-CI/CD-2088FF?logo=githubactions&logoColor=white" alt="GitHub Actions">
</p>

<p align="center">
  <a href="https://sbh.howon.me/">서비스 콘솔</a> ·
  <a href="https://app.notion.com/p/3ed8bee9ada4809eb9bcc5fdd1f07082">최종 발표</a> ·
  <a href="https://github.com/softbank-hackathon-2026">원본 Organization</a>
</p>

> **SoftBank Hackathon 2026 in Korea · 예선 · Team Freesia**<br>
> 이 저장소는 팀 Organization의 저장소들을 git submodule로 묶은 모음 저장소입니다.

## 저장소 구성

```bash
git clone --recurse-submodules <this-repo-url>
```

| 경로 | 원본 저장소 | 내용 |
|---|---|---|
| `frontend/` | [Freesia-Frontend](https://github.com/softbank-hackathon-2026/Freesia-Frontend) | 관리 콘솔(React), API 연동, 화면 검증 |
| `backend/` | [Freesia-backend](https://github.com/softbank-hackathon-2026/Freesia-backend) | 앱·인프라·분석·배포·모니터링 API(FastAPI) |
| `infra/platform-terraform/` | [platform-terraform](https://github.com/softbank-hackathon-2026/platform-terraform) | 플랫폼의 AWS 기반 인프라 |
| `infra/workload-terraform/` | [workload-terraform](https://github.com/softbank-hackathon-2026/workload-terraform) | 고객 앱을 위한 기반 환경 |
| `infra/workload-deploy/` | [workload-deploy](https://github.com/softbank-hackathon-2026/workload-deploy) | AWS·온프레미스 앱 실행·정리 워크플로와 템플릿 |
| `samples/sample-shop/` | [sample-shop](https://github.com/softbank-hackathon-2026/sample-shop) | 배포 시연용 샘플 앱 |
| `samples/shop-api/` | [shop-api](https://github.com/softbank-hackathon-2026/shop-api) | 배포 시연용 샘플 API |

## 주요 기능

| 기능 | 내용 |
|---|---|
| **서비스별 환경 선택** | 인프라 담당자가 준비한 Infra Space를 서비스명으로 선택 |
| **저장소 연결과 AI 추천** | 공개 GitHub 저장소를 분석해 실행 환경 후보와 설정값 추천(Amazon Bedrock) |
| **배포 구성 검토** | 선택한 템플릿에 들어갈 구성을 배포 전에 검토 |
| **AWS·온프레미스 배포** | GitHub Actions로 AWS는 Terraform, 온프레미스는 Ansible 실행 |
| **배포 결과 관찰** | SSE 진행 상태, 자원 트리, CloudWatch 로그·지표 |

## 아키텍처

<img src="https://raw.githubusercontent.com/softbank-hackathon-2026/.github/main/assets/architecture/system.svg" alt="React 관리 콘솔 → FastAPI 제어 서버 → GitHub Actions → AWS·온프레미스 고객 앱" width="100%">

<img src="https://raw.githubusercontent.com/softbank-hackathon-2026/.github/main/assets/architecture/infrastructure.png" alt="CloudFront, Private VPC의 Internal ALB·ECS Fargate·RDS, 온프레미스 연결" width="100%">

## 기술 스택

| 영역 | 주요 기술 |
|---|---|
| **Frontend / Backend** | React, TypeScript, Vite / Python, FastAPI, SQLAlchemy, PostgreSQL |
| **AWS** | CloudFront, S3, ALB, ECS Fargate, ECR, RDS, EC2, Lambda, IAM, Bedrock, CloudWatch |
| **자동화 / 하이브리드** | GitHub Actions, Docker, Terraform, Ansible, Cloudflare Tunnel, Proxmox |
| **테스트** | pytest, Playwright |

## 본인 담당

**박소정 ([@sojjeoi](https://github.com/sojjeoi)) · DevOps / CI/CD**

## 상세 문서

[CI/CD](https://github.com/softbank-hackathon-2026/.github/blob/main/docs/cicd.md) ·
[인프라 상세](https://github.com/softbank-hackathon-2026/.github/blob/main/docs/infrastructure.md) ·
[AWS Organizations](https://github.com/softbank-hackathon-2026/.github/blob/main/docs/aws-organizations.md) ·
[AI 추천 과정](https://github.com/softbank-hackathon-2026/.github/blob/main/docs/ai-recommendation.md) ·
[모니터링](https://github.com/softbank-hackathon-2026/.github/blob/main/docs/monitoring.md)
