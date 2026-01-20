# Kira-Toolkit

Hardened Kira development standards and patterns for safe, consistent, and maintainable functional code. Designed to work with Claude Code/AI and agentic development.

**Version**: 0.1.0 (Initial Release)

## What is Kira-Toolkit?

Kira-Toolkit provides coding standards, rules, and commands for developing in Kira—a functional programming language designed for AI code generation. It enforces:

- **Pure functions by default** with explicit effect tracking
- **Exhaustive pattern matching** for safe data handling
- **Algebraic data types** for robust data modeling
- **Higher-order function patterns** for composable code
- **Explicit types everywhere** with no inference

## Quick Start

### Install in Your Project

```
/kira-install
```

This command:
1. Clones Kira-Toolkit into your project
2. Copies rules and commands to `.claude/`
3. Sets up version tracking

### Available Commands

| Command | Purpose |
|---------|---------|
| `/kira-init` | Create a new Kira-Toolkit project |
| `/kira-install` | Install Kira-Toolkit into existing project |
| `/kira-review` | Review code against standards |
| `/kira-safety` | Security-focused code review |
| `/kira-check` | Run build, tests, and checks |
| `/kira-update` | Update to latest Kira-Toolkit |

## Documentation

- **[KIRATOOLKIT.md](KIRATOOLKIT.md)** - Quick reference guide
- **[STANDARDS.md](STANDARDS.md)** - Comprehensive coding standards
- **[docs/patterns/](docs/patterns/)** - Pattern guides
- **[docs/security/](docs/security/)** - Security guides

## Key Kira Features

Kira is the functional sibling to Klar. Key characteristics:

### Pure by Default

```kira
// Pure function - no side effects allowed
let add: fn(i32, i32) -> i32 = fn(a: i32, b: i32) -> i32 {
    return a + b
}

// Effect function - can perform IO
effect fn main() -> IO[void] {
    std.io.println("Hello, Kira!")
    return
}
```

### Algebraic Data Types

```kira
// Sum type
type Option[T] =
    | Some(T)
    | None

// Product type
type Point = {
    x: f64,
    y: f64
}
```

### Pattern Matching

```kira
let describe: fn(Option[i32]) -> string = fn(opt: Option[i32]) -> string {
    var result: string
    match opt {
        Some(n) => { result = "has value: {n}" }
        None => { result = "empty" }
    }
    return result
}
```

### Higher-Order Functions

```kira
let doubled: List[i32] = map[i32, i32](
    numbers,
    fn(x: i32) -> i32 { return x * 2 }
)
```

## Why Kira-Toolkit?

1. **AI-Optimized**: Standards designed for clear AI code generation
2. **Type Safety**: Explicit types prevent ambiguity
3. **Effect Tracking**: Know exactly what code can do IO
4. **Pattern Safety**: Exhaustive matching prevents runtime errors
5. **Consistent Style**: One way to write each construct

## Kira vs Klar

| Aspect | Klar | Kira |
|--------|------|------|
| Paradigm | Imperative | Functional |
| Mutation | `var` for mutable | Immutable in pure code |
| Default | Effectful | Pure |
| Effects | Implicit | Explicit in types |
| Data | Structs + mutation | Algebraic data types |

## License

MIT License - See [LICENSE](LICENSE) for details.

## Contributing

Kira-Toolkit is designed to evolve with the Kira language. Contributions welcome for:
- New patterns and best practices
- Security guidance
- Testing patterns
- Documentation improvements
