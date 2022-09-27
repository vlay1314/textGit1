# threejs3D-
#这是使用threejs框架进行一个简单的demo展示，实现纹理贴图进行交互，通过射线相交计算当前选中的物体来进行判断操作，
#实现了点击模型弹出文本框显示相关信息，点击不同模型进行场景切换。
// 监听鼠标移动事件，这里修改摄像机的x,y的旋转方向就会让整个模型都左右上下旋转，注释掉x方向的话就可以实现左右环绕观看；  
  `window.addEventListener(
    "mousemove",
    (e) => {
      if (isMouseDown) {
       camera.rotation.y += (e.movementX / window.innerWidth) * Math.PI;
        camera.rotation.x += (e.movementY / window.innerHeight) * Math.PI;
      }
    },
    false
  );`  
  这里是不使用这个鼠标移动监听的话，可以使用控制器，把这段注释去掉  
  `// 添加控制器
  // controls = new OrbitControls(camera, renderer.domElement);
  // controls.enableDamping = true;
  // controls.target.set(0, 0, 0);`  
![image](https://github.com/vlay1314/threejs3D-/blob/main/iShot_2022-09-27_10.24.33.gif)

![image](https://github.com/vlay1314/threejs3D-/blob/main/iShot_2022-09-27_10.40.03.gif)
