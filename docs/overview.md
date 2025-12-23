# Frost Anchorline — Overview

Frost Anchorline is a Base-first project designed with clarity, minimal configuration,
and predictable network behavior in mind.

This document provides a high-level overview for contributors and maintainers.

---

## Purpose

The project focuses on:
- Operating natively on **Base Mainnet** and **Base Sepolia**
- Using static configuration for all network-related data
- Keeping runtime logic free from hardcoded chain metadata

All chain-specific details should live in configuration files, not in source code.

---

## Architecture Principles

- **Config-first**  
  Network metadata (chainId, RPC URLs, explorers) is defined in JSON configs.

- **Minimal surface area**  
  Only required networks are supported to reduce complexity and risk.

- **Base-aligned**  
  Dependencies, tooling, and assumptions should align with the Base ecosystem.

---

## Network Support

Supported networks:
- Base Mainnet (`chainId: 8453`)
- Base Sepolia (`chainId: 84532`)

Network selection should be deterministic and derived from configuration defaults
or explicit user/environment choice.

---

## Conventions

- File and folder names use **lowercase** and **kebab-case**
- Config files are placed under `config/`
- Documentation lives under `docs/`
- No secrets or API keys are committed to the repository

---

## Contribution Notes

Before opening a PR:
- Ensure network changes are reflected in config files
- Avoid duplicating chain IDs or RPC URLs in code
- Keep documentation concise and up to date

---

_Last updated: initial overview_
