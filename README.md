# slo_blame_chain_signature_match

**给自动驾驶规划控制专家·SLO 违约的归因链路算一个特征指纹并定位可疑片段。**

`slo_blame_chain_signature_match` —— 通过字符级与结构级特征识别自动驾驶规划控制专家·SLO 违约的归因链路的痕迹，给出密度与命中位置

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`slo_blame_chain_signature_match.py` 拷走就能用
- 不联网、不写文件

## 对应的岗位

- 目标岗位：**生数科技 · 初级自动驾驶规划控制专家**
- 技能主线：自动驾驶、强化学习、具身智能
- 领域标签：自动驾驶
- 研究方向：自动驾驶规划控制专家·SLO 违约的归因链路

工具里的规则表就是照着上面这条岗位要求建的——每条规则都挂在技能线或领域标签上，命中时能指回具体要求。

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install brandshow4-slo_blame_chain_signature_match
```

装完直接用命令名调用：

```bash
slo_blame_chain_signature_match --help
```

也可以不用安装，直接把 `slo_blame_chain_signature_match.py` 拷走用——它只依赖标准库。

## 为什么需要它

只做特征匹配不做语义判定，所以不会被同义改写绕过

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到岗位要求的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python slo_blame_chain_signature_match.py --file input.txt
python slo_blame_chain_signature_match.py --text "示例内容"
python slo_blame_chain_signature_match.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 相似度按字符与词估算，不等于向量相似度。
- 不联网，不做语义检索。

## 跑测试

```bash
python test_slo_blame_chain_signature_match.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/brandshow4/slo_blame_chain_signature_match>

---

## 关于作者

brandshow4 做自动驾驶规划控制专家·SLO 违约的归因链路相关的问题，方向对标生数科技的初级自动驾驶规划控制专家岗位。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://brandshow4.github.io>
- 仓库：<https://github.com/brandshow4/slo_blame_chain_signature_match>

## 许可

MIT，见 [LICENSE](LICENSE)。
