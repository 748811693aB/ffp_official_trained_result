# ffp_official_trained_result
完全按照ffp官方代码、方法训练并测试模型效果
- 4号服务器保存路径：~/Desktop/HXB/F_Pointpillar/05-15
train.py比原版增加：
```
#HXB 消除置信度低的
                if score>0.3:
                    result_lines.append(result_line)
```
