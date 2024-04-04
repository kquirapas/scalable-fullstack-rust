# Software Architecture Case Study with Rust

# Workspace Structure

## Phase 1: 1 Binary

- Each Rust library is a separate service with a connecting `.rs.` file at `/root` which will serve as the eventual `main.rs` or `entrypoint` for containerizing in phase 2.

```
/root
    /frontend
        lib.rs
    /gateway
        lib.rs
    /event
        lib.rs
    /account.rs
        lib.rs
    /post.rs
        lib.rs
    /comment.rs
        lib.rs
    /persistence
        lib.rs
    frontend.rs
    gateway.rs 
    event.rs
    account.rs
    post.rs
    comment.rs
    persistence.rs

    main.rs
```

## Phase 2: Separated into containerized services

```
/root
    [CONTAINER]
    frontend.rs => main()
    /frontend
        lib.rs

    [CONTAINER]
    gateway.rs => main()
    /gateway
        lib.rs

    [CONTAINER]
    event.rs => main()
    /event
        lib.rs

    [CONTAINER]
    account.rs => main()
    /account.rs
        lib.rs

    [CONTAINER]
    post.rs => main()
    /post.rs
        lib.rs

    [CONTAINER]
    comment.rs => main()
    /comment.rs
        lib.rs

    [CONTAINER]
    persistence.rs => main()
    /persistence
        lib.rs
```

# Skill Objectives
1. Fullstack
2. Docker
3. Kubernetes
4. Grafana / Prometheus

# Software Architecture Objectives
1. Scalable (Decoupled)
2. Event-Driven Architecture
3. Hexagonal / Ports and Adapters Architecture (App Layer)
5. Onion Architecture (Presentation, Infra, Application, Domain)

