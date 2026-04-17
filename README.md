# 📘 PES-VCS Lab Report

## 👤 Student Details
- Name: Manoj Gaonkar
- SRN: PES1UG25CS827

---

## 📌 Project Overview

This project implements a simplified Version Control System (VCS) similar to Git.  
It tracks file changes, stores snapshots efficiently, and maintains commit history.

Key concepts used:
- Content-addressable storage (SHA-256)
- Tree structures for directories
- Commit linking (history tracking)
- Index (staging area)

---

## ⚙️ Phase 1: Object Storage

### 🔹 Implementation
Implemented:
- `object_write()` → stores objects using SHA-256 hashing
- `object_read()` → retrieves and verifies stored objects

### 🔹 Key Concepts
- Deduplication (same content = same hash)
- Integrity check using hashing
- Directory sharding

---

## 🌳 Phase 2: Tree Objects

### 🔹 Implementation
Implemented:
- `tree_from_index()` → builds directory structure from index

### 🔹 Key Concepts
- Recursive directory handling
- Tree representation of filesystem
- Deterministic serialization

---

## 📂 Phase 3: Index (Staging Area)

### 🔹 Implementation
Implemented:
- `index_load()` → loads index file
- `index_save()` → saves index atomically
- `index_add()` → stages files

### 🔹 Key Concepts
- File tracking
- Metadata storage (mtime, size)
- Change detection

---

## 🧾 Phase 4: Commit System

### 🔹 Implementation
Implemented:
- `commit_create()` → creates commit objects and updates HEAD

### 🔹 Key Concepts
- Snapshot-based versioning
- Parent commit linking
- Branch reference updates

---

## 💻 Commands Used

```bash
make
./pes init
./pes add file1.txt
./pes commit -m "Initial commit"
./pes log
