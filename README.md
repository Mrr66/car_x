[![Build Status](https://github.com/Mrr66/car_x/blob/main/carone.jpg?raw=true)](https://travis-ci.org/joemccann/dillinger)
# Speed Car
## Crie sua competição com outros jogadores


[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

🚗 O Speed Car é um jogo de corrida simples e leve que roda em seu PC e celular

- Escolha o seu carro
- Escolha a cor
- ✨ Jogue quando quiser
## Features

- REACT
- Firebase
- LocalStorage
- Drag and drop
- Audio mp3 e graficos 2d

## Instalação
#### * Basta fazer o git clone
## Build 

```js
{
  "hosting": {
    "public": "build",
    "ignore": [],
    "rewrites": [
      {
        "source": "**",
        "destination": "/index.html"
      }
    ]
  }
}
```

## Parametros do carro

```js
const wheelInfo = {
    radius,
    directionLocal: [0, -1, 0],
    axleLocal: [1, 0, 0],
    suspensionStiffness: 60,
    suspensionRestLength: 0.1,
    frictionSlip: 5,
    dampingRelaxation: 2.3,
    dampingCompression: 4.4,
    maxSuspensionForce: 100000,
    rollInfluence: 0.01,
    maxSuspensionTravel: 0.1,
    customSlidingRotationalSpeed: -30,
    useCustomSlidingRotationalSpeed: true,
  };
```

## Executando o carro
```js
export function Car() {
  const modelsFolderPath = `${process.env.PUBLIC_URL}/`;
  const modelFileName  = "car_model_gti.glb";
  const modelFilePath = `${modelsFolderPath}${modelFileName}`;
  const mesh = useLoader(
    GLTFLoader,
    modelFilePath,
  ).scene;

  useEffect(() => {
    if (!mesh) return;
    mesh.scale.set(0.0012, 0.0012, 0.0012); 
    mesh.children[0].position.set(-365, -18, -67);
    mesh.scale.set(0.2, 0.2, 0.2); 
    mesh.children[0].position.set(-4, 0.37, -11);
  }, [mesh]);

  return (
    <primitive object={mesh} rotation-y={Math.PI/1.5} />
  );
}
```

## Development 
Este projeto não permite múltiplos jogadores, fique a vontade para modificar
[![Build Status](https://github.com/Mrr66/car_x/blob/main/car_2.jpg?raw=true)](https://travis-ci.org/joemccann/dillinger)
