# ffp_official_trained_result
完全按照ffp官方代码、方法训练并测试模型效果
- 4号服务器保存路径：~/Desktop/HXB/F_Pointpillar/05-15
- 运行检测的指令：(ZC2_pointpillars) whut-4@whut4:~/Desktop/HXB/F_Pointpillar/05-15/Frustum-Pointpillars/second$ python pytorch/train.py evaluate --config_path=/home/whut-4/Desktop/HXB/F_Pointpillar/05-15/Frustum-Pointpillars/second/configs/pointpillars/car/xyres_16.proto --model_dir=/home/whut-4/Desktop/HXB/F_Pointpillar/05-15/Frustum-Pointpillars/second/ckpt/frustum_pp_car
- 2023-7-31根据KINS数据集训练的YOLOV8X-seg.pt过滤的点云按照FPP数据集生成，保存在：/home/whut-4/Desktop/HXB/F_Pointpillar/07-31/KITTI_DATASET_ROOT

- AP@
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/09f446e4-bbef-4987-9d3e-e27842805e0c)

- 可视化效果
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/0c8086ef-0b31-4ded-8440-5cf62e85b5df)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/87bfe5a4-9b7f-4d09-9d8b-437d5a3f2722)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/4a973fa3-6dfa-44ea-a27c-34b70dc191ad)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/600c1bbc-9db0-4634-91f9-4e07b3c086df)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/e3a0b7ec-611c-4c26-99ad-5af2f50894b5)

## 2023-7-31测试
```
File "utils/eval.py", line 131:
@numba.jit(nopython=True, parallel=True)
def d3_box_overlap_kernel(boxes, qboxes, rinc, criterion=-1):
^

  state.func_ir.loc))
Car AP@0.70, 0.70, 0.70:
bbox AP:90.65, 87.32, 82.42
bev  AP:89.80, 81.65, 78.17
3d   AP:81.91, 70.83, 65.85
aos  AP:90.01, 85.01, 79.67
Car AP@0.70, 0.50, 0.50:
bbox AP:90.65, 87.32, 82.42
bev  AP:90.89, 90.68, 88.17
3d   AP:90.88, 90.56, 87.58
aos  AP:90.01, 85.01, 79.67

Car coco AP@0.50:0.05:0.95:
bbox AP:70.40, 66.61, 63.92
bev  AP:69.32, 64.91, 61.22
3d   AP:58.25, 53.24, 50.03
aos  AP:69.93, 64.96, 61.85
```
