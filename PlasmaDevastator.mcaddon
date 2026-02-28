PlasmaDevastator/
│
├── behavior_packs/
│   └── PlasmaDevastator_BP/
│       ├── manifest.json
│       ├── items/
│       │   └── railgun.json
│       └── entities/
│           └── plasma_projectile.json
│
└── resource_packs/
    └── PlasmaDevastator_RP/
        ├── manifest.json
        ├── textures/
        │   ├── item_texture.json
        │   └── items/
        │       └── railgun.png        ← your railgun texture
        │
        ├── particles/
        │   ├── beam_trail.json
        │   ├── shockwave.json
        │   ├── distortion.json
        │   └── blackhole.json
        │
        ├── sounds/
        │   └── plasma_fire.ogg        ← your sound file
        │
        └── sounds.json
        {
  "format_version": 2,
  "header": {
    "name": "Plasma Devastator BP",
    "description": "Mythic Sci-Fi Railgun",
    "uuid": "5a1c7a10-3d7e-4c5a-91e2-111111111111",
    "version": [1,0,0],
    "min_engine_version": [1,20,0]
  },
  "modules": [
    {
      "type": "data",
      "uuid": "8b2c8e20-4e8f-4d6b-92f3-222222222222",
      "version": [1,0,0]
    }
  ]
}
{
  "format_version": 2,
  "header": {
    "name": "Plasma Devastator BP",
    "description": "Mythic Sci-Fi Railgun",
    "uuid": "5a1c7a10-3d7e-4c5a-91e2-111111111111",
    "version": [1,0,0],
    "min_engine_version": [1,20,0]
  },
  "modules": [
    {
      "type": "data",
      "uuid": "8b2c8e20-4e8f-4d6b-92f3-222222222222",
      "version": [1,0,0]
    }
  ]
}
{
  "format_version": "1.20.0",
  "minecraft:item": {
    "description": {
      "identifier": "plasma:railgun",
      "category": "equipment"
    },
    "components": {
      "minecraft:max_stack_size": 1,
      "minecraft:icon": {
        "texture": "railgun"
      },
      "minecraft:use_animation": "bow",
      "minecraft:use_duration": 40,
      "minecraft:shooter": {
        "projectile": "plasma:projectile",
        "launch_power": 4,
        "max_draw_duration": 40,
        "charge_on_draw": true,
        "ammunition": [
          { "item": "minecraft:arrow" }
        ]
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:entity": {
    "description": {
      "identifier": "plasma:projectile",
      "is_spawnable": false,
      "is_summonable": false
    },
    "components": {
      "minecraft:projectile": {
        "gravity": 0,
        "power": 3,
        "particle": "plasma:beam_trail",
        "on_hit": {
          "impact_damage": {
            "damage": 50,
            "knockback": true
          },
          "run_command": {
            "command": [

              "playsound plasma.fire @a[r=40] ~ ~ ~ 1 0.6",

              "particle plasma:blackhole ~ ~ ~",
              "effect @e[r=10] slowness 2 4 true",
              "tp @e[r=8] ~ ~ ~ facing @s",

              "camera shake add @a[r=15] 0.8 0.5",

              "summon lightning_bolt ~1 ~ ~",
              "summon lightning_bolt ~-1 ~ ~",
              "summon lightning_bolt ~ ~ ~1",
              "summon lightning_bolt ~ ~ ~-1",

              "particle plasma:shockwave ~ ~ ~",
              "particle plasma:distortion ~ ~ ~",
              "particle minecraft:huge_explosion_emitter ~ ~ ~",

              "effect @e[r=10] blindness 5 1 true",
              "effect @e[r=10] nausea 5 1 true",

              "camera shake add @a[r=20] 1.5 0.7"
            ]
          }
        }
      }
    }
  }
}
{
  "format_version": 2,
  "header": {
    "name": "Plasma Devastator RP",
    "description": "Textures, particles, sounds",
    "uuid": "9c3d9f30-5f9a-4e7c-a3f4-333333333333",
    "version": [1,0,0],
    "min_engine_version": [1,20,0]
  },
  "modules": [
    {
      "type": "resources",
      "uuid": "ad4ea040-6fab-4f8d-b4f5-444444444444",
      "version": [1,0,0]
    }
  ]
}
{
  "resource_pack_name": "PlasmaDevastator_RP",
  "texture_name": "atlas.items",
  "texture_data": {
    "railgun": {
      "textures": "textures/items/railgun"
    }
  }
}
{
  "format_version": "1.10.0",
  "particle_effect": {
    "description": {
      "identifier": "plasma:beam_trail",
      "basic_render_parameters": {
        "material": "particles_add",
        "texture": "textures/particle/particles"
      }
    },
    "components": {
      "minecraft:emitter_rate_steady": { "spawn_rate": 120 },
      "minecraft:particle_lifetime_expression": { "max_lifetime": 0.2 },
      "minecraft:particle_appearance_tinting": {
        "color": [0.2, 0.9, 1.0, 1.0]
      }
    }
  }
}
{
  "format_version": "1.10.0",
  "particle_effect": {
    "description": {
      "identifier": "plasma:shockwave",
      "basic_render_parameters": {
        "material": "particles_add",
        "texture": "textures/particle/particles"
      }
    },
    "components": {
      "minecraft:emitter_rate_instant": { "num_particles": 80 },
      "minecraft:particle_lifetime_expression": { "max_lifetime": 0.6 }
    }
  }
}
{
  "format_version": "1.10.0",
  "particle_effect": {
    "description": {
      "identifier": "plasma:distortion",
      "basic_render_parameters": {
        "material": "particles_alpha",
        "texture": "textures/particle/particles"
      }
    },
    "components": {
      "minecraft:emitter_rate_instant": { "num_particles": 20 },
      "minecraft:particle_lifetime_expression": { "max_lifetime": 0.3 }
    }
  }
}
{
  "format_version": "1.10.0",
  "particle_effect": {
    "description": {
      "identifier": "plasma:blackhole",
      "basic_render_parameters": {
        "material": "particles_add",
        "texture": "textures/particle/particles"
      }
    },
    "components": {
      "minecraft:emitter_rate_instant": { "num_particles": 120 },
      "minecraft:particle_lifetime_expression": { "max_lifetime": 0.8 },
      "minecraft:particle_appearance_tinting": {
        "color": [0.05, 0.1, 0.2, 1.0]
      }
    }
  }
}
{
  "plasma.fire": {
    "sounds": [
      {
        "name": "sounds/plasma_fire",
        "volume": 1
      }
    ]
  }
}
