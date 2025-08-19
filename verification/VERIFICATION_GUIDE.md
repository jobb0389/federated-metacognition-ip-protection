# Verification Guide

## How to Verify IP Protection Proofs

### Prerequisites
- GPG/GnuPG installed
- Git (optional, for commit verification)

### Step 1: Import Public Key
Import James O'Brien-Brown's public key:
`
gpg --import GPG_PUBLIC_KEY.asc
`

### Step 2: Verify Proof Signatures
For each proof in the proofs/ directory:
`
gpg --verify manifest.json.asc manifest.json
`

### Step 3: Verify Chain Integrity
Each manifest contains:
- ChainIndex: Sequential number
- PreviousHash: Links to previous manifest
- SHA256: Content hash
- CommitHash: Git commit reference

### Step 4: Cross-Reference with GitHub
Compare hashes with:
https://github.com/jobb0389/jobb_federated_metacognition_framework

### Expected Output
Good signature from "James O'Brien-Brown <jobb0389@gmail.com>"

### Trust Levels
- Ultimate: Direct verification with author
- Full: Multiple independent verifications
- Marginal: Single verification
- Unknown: Not yet verified
