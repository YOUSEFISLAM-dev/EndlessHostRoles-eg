
# EndlessHostRoles-eg Security Threat Model

## Project
A security-focused fork of EndlessHostRoles, an Among Us
mod implemented in C# using BepInEx.

## Primary security objectives
- Prevent malicious or malformed input from causing crashes.
- Identify unsafe handling of network messages and game state.
- Detect authorization and trust-boundary mistakes.
- Find unsafe file operations, deserialization, and process execution.
- Identify exposed credentials, insecure update mechanisms,
  and vulnerable dependencies.

## Audit priorities
1. Network message parsing and validation.
2. Host/client trust boundaries and game-state synchronization.
3. Input validation and exception handling.
4. File system operations and external process execution.
5. Dependency and build configuration security.

## Scope
Audit the source code and dependencies in this repository.
Distinguish confirmed vulnerabilities from theoretical risks.
Include reproduction steps, affected files, impact, and a
minimal proposed fix for each confirmed finding.

Do not assume that every client can execute host-only code.
Verify reachability and attacker-controlled inputs before
assigning severity.
