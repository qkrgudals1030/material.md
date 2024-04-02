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
