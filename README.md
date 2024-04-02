### part1 실습화면

![image](https://github.com/qkrgudals1030/material.md/assets/50895124/1fb9d14b-6bb1-4a87-8346-09cda706bb31)

![image](https://github.com/qkrgudals1030/material.md/assets/50895124/340c8a2c-8ca2-4887-8b5c-8f150ba5ecda)


### part1 코드 변경 부분
```
 _setupModel(){
       const vertices = [];
       for(let i = 0; i < 10000; i++) {
        const x = THREE.MathUtils.randFloatSpread(5);
const y = THREE.MathUtils.randFloatSpread(5);
const z = THREE.MathUtils.randFloatSpread(5);

        vertices.push(x,y,z);
       }

       const geometry = new THREE.BufferGeometry();
       geometry.setAttribute(
        "position",
        new THREE.Float32BufferAttribute(vertices, 3)
       );
       const material = new THREE.PointsMaterial({
        color: "yellow",
        size: 10,
        sizeAttenuation: false
       });
       const points = new THREE.Points(geometry, material);
       this._scene.add(points);
    }
```
```
_setupModel(){
        const vertices = [
            -1, 1, 0,
            1, 1, 0,
            -1, -1, 0,
            1, -1, 0,
        ];
        
        const geometry = new THREE.BufferGeometry();
        geometry.setAttribute(
         "position",
         new THREE.Float32BufferAttribute(vertices, 3)
        );
        const material = new THREE.LineDashedMaterial({
            color: 0x00fffff,
            dashSize: 0.2,
            gapSize: 0.1,
            scale: 4
     });
     const line = new THREE.LineLoop(geometry, material);
     line.computeLineDistances();
     this._scene.add(line);
    }

```    
### part2 실습화면

![image](https://github.com/qkrgudals1030/material.md/assets/50895124/168b5064-3032-45cf-b256-0e602664c7f5)


### part2 코드 변경 부분
```
 _setupModel(){
        const material = new THREE.MeshPhysicalMaterial({
            color : 0x00ffff,
            emissive: 0x00000,
            roughness: 1,
            metalness:0,
            clearcoat: 1,
            clearcoatRoughenss: 0,
            wireframe: false,
            flatShading: false,
        });
```        
### part3
### part3 코드 변경 부분
### part4
### part4 코드 변경 부분


### 소감

유튜브 영상을 보고 직접 따라 코드를 변경해보면서 쉽게 실습을 이어 날갈 수 있었고 막히는 부분이 생긴다면 챗지피티나 혹은 친구들에게 도움을 얻어 해결해 보면서 서로의 부족한 부분을 채우는 식으로 진행해보았습니다. 이런식으로 실습을 하다보니 코딩에대해서 더 꼼꼼하게 보고 더 확실하게 해볼 수 있는 기회였던거 같습니다. 또한 따라친 코드가 작동되는 것에 기뻐하는것이 아니라 제가 변경한 부분이 반영되어 프로그램이 실행되었을 때 실습의 재미를 느낄 수 있었습니다. 이를 통해 저만의 작품을 제작하여 다른사람들에게 영감을 줄 수 있으면 좋겠다고 생각하게 되었고 그래픽스 수업을 더 열심히 들어 저만의 작품을 만들 수 있도록 해볼 것입니다. ai그래픽스 화이팅
