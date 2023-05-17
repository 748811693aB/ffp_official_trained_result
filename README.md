# ffp_official_trained_result
完全按照ffp官方方法训练并测试模型效果
- 4号服务器保存路径：~/Desktop/HXB/F_Pointpillar/05-15
train.py比原版增加：
```
#HXB 消除置信度低的
                if score>0.3:
                    result_lines.append(result_line)
```
- 运行检测指令：
```
(ZC2_pointpillars) whut-4@whut4:~/Desktop/HXB/F_Pointpillar/05-15/Frustum-Pointpillars/second$ 
python pytorch/train.py evaluate --config_path=configs/pointpillars/car/xyres_16.proto --model_dir=ckpt/frustum_pp_car/
```
- 准确度：
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/27625649-b5fc-4c14-9f9f-9c3e9781f21f)

- 可视化效果
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/d1aae3e8-4dc0-4746-8236-ee3c533d7a1f)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/72820461-e1b8-48df-920f-1270ebc0c5ca)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/4f4bbc3b-e70a-4acc-9453-b1f78ab1ed3f)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/a94bdfd2-98fa-45b5-a5a0-3fe1c46e608b)
![image](https://github.com/748811693aB/ffp_official_trained_result/assets/102968155/0ebec638-2eaf-4dde-9960-79c57d50e004)
