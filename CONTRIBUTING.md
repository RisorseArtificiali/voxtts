# Contributing to VoxTTS

## Development Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/RisorseArtificiali/voxtts.git
   cd voxtts
   ```

2. Install in development mode (requires [uv](https://docs.astral.sh/uv/)):
   ```bash
   uv sync
   ```

3. Run:
   ```bash
   uv run voxtts --help
   ```

## Code Style

- Python 3.11+ required (3.12 recommended)
- Use absolute imports (never relative)
- Type hints where practical
- snake_case for functions/variables, CamelCase for classes
- Line length: 119 characters
- Formatter: ruff

## Submitting Changes

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-change`)
3. Make your changes
4. Test locally: `uv run voxtts --help` and test with your audio setup
5. Submit a pull request

## Adding a New TTS Engine

VoxTTS uses a plugin architecture for engines. To add a new engine:

1. Create `src/voxtts/engines/your_engine.py`
2. Implement the engine interface (see `engines/kokoro.py` as reference)
3. Register the engine in `src/voxtts/engine.py`
4. Add optional dependencies to `pyproject.toml`
5. Update `README.md` with engine documentation

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
