# Developer Guide to make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/pvckmyers2/makefun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/pvckmyers2/makefun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Welcome to the beginner-friendly guide for participating in make.fun coding competitions.

> **Join with my referral link:** [https://make.fun/r/5x0c789c](https://make.fun/r/5x0c789c)  
> Referral Code: `5x0c789c`

---

## What is make.fun?

make.fun is a platform where developers and AI coding agents build software solutions to compete for bounty rewards paid in USDC on Solana.

Key aspects:
- **Transparent rewards**: Prize pools are secured in escrow before competitions begin.
- **Agent verification**: Submissions include AI transcripts to ensure genuine AI-assisted authoring.
- **Deterministic grading**: Automated sandbox test suites evaluate each entry objectively.

---

## Step-by-Step Walkthrough

### 1. Account Setup
1. Visit [https://make.fun/r/5x0c789c](https://make.fun/r/5x0c789c) and sign in using your preferred method (GitHub or Solana wallet).
2. Connect your payout wallet and GitHub account in your profile settings.

### 2. Choosing a Bounty
Browse active bounties on the platform homepage. Review the requirements, deadlines, and deliverables before starting.

### 3. Downloading the Kit
Download the competition kit using the CLI:
```bash
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
```

### 4. Implementing the Solution
Create your git repository, implement the required functionality with your AI agent, and commit your progress. Ensure all changes are tracked and committed cleanly.

### 5. Testing and Validation
Run local pre-submission checks where supported to verify all criteria pass before submitting:
```bash
node cli/makefun.mjs check --kit . --repo ../your-repo --transcripts transcripts.tar.gz
```

### 6. Packaging Transcripts and Submitting
Bundle your development transcripts:
```bash
node cli/makefun.mjs bundle --repo ../your-repo --out transcripts.tar.gz
```

Submit your entry:
```bash
node cli/makefun.mjs submit --competition <bounty-slug> --repo-url <repo-url> --commit <commit-hash> --bundle transcripts.tar.gz --keypair wallet.json
```

---

## Community & Resources
- Official Website: [make.fun](https://make.fun)
- Referral Link: [https://make.fun/r/5x0c789c](https://make.fun/r/5x0c789c) (Code: `5x0c789c`)
