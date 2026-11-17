# Áudio em Jogo 2D - Unity

Projeto simples em Unity 2D com música de fundo em looping e efeitos sonoros ligados às mecânicas do personagem, todos tocados pelo componente `AudioSource`.

**Versão do Unity:** 6000.3.25f1

## Enunciado

Construa um projeto na Unity (temática e conteúdo livre) que utilize o componente de AudioSource para a emissão de uma música (em looping) e de efeitos sonoros. Os efeitos sonoros devem acontecer quando alguma mecânica no jogo é executada (por exemplo: um pulo de um personagem; passos que ele dá quando anda; um ataque que atinge um inimigo; um som emitido quando o player ou o inimigo morre…).

## Funcionalidades

- **Música de fundo:** o objeto `Musica` tem um `AudioSource` com _Loop_ e _Play On Awake_ ativados, tocando `Winds of Valor`.
- **Efeitos sonoros:** o personagem (`HeroKnight`) tem um `AudioSource` próprio e toca cada som com `PlayOneShot` no momento da mecânica.

## Controles

| Tecla           | Ação                       | Som                                  |
| --------------- | -------------------------- | ------------------------------------ |
| `A` / `D`       | Andar                      | `footstep.wav` (passos, a cada 0,3s) |
| `Espaço`        | Pular                      | `footstep.wav` (mais agudo)          |
| Clique esquerdo | Atacar                     | `sword.wav`                          |
| `Q`             | Tomar dano                 | `pain.wav`                           |
| `E`             | Morrer                     | `DeathExplosion.wav`                 |
| `R`             | Reviver (depois de morrer) | —                                    |
| `Shift`         | Rolar                      | —                                    |
| Clique direito  | Defender                   | —                                    |

Depois de morrer, o personagem não se mexe até ser revivido com `R`.

## Cenas

| Cena            | Descrição                                 |
| --------------- | ----------------------------------------- |
| `CenaPrincipal` | Cena do jogo (índice 0 no Build Settings) |

## Como executar

1. Abra o projeto no Unity.
2. Abra a cena `Assets/Scenes/CenaPrincipal`.
3. Clique em **Play**.
4. Use os controles acima para ouvir os efeitos sonoros.

## Estrutura

```
Assets/
├── Scenes/
│   └── CenaPrincipal.unity
├── Scripts/
│   ├── HeroKnight.cs
│   ├── Sensor_HeroKnight.cs
│   └── DestroyEvent_HeroKnight.cs
└── Assets/
    ├── Hero Knight - Pixel Art/              (personagem e cenário)
    ├── Dark Knight/Sounds/                   (efeitos sonoros)
    └── 10 Fantasy Medieval Ambient Tracks/   (música)
```

## Assets utilizados (Unity Asset Store)

- **Hero Knight - Pixel Art** (Sven Thole): personagem, animações e cenário.
- **Dark Knight 2D - Animated Character + VFX** (TealFalcon): efeitos sonoros.
- **Free 10 Medieval Ambient Fantasy Tracks** (alkakrab): música de fundo.
