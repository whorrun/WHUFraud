武汉大学疑似学术不端证据共享仓库  
（WHU-Misconduct-Evidence Repo – 中文规范）

1. 定位  
本仓库仅针对“署名单位或通信地址含『武汉大学』(Wuhan University, WHU)”的论文、专著、科研报告等公开作品所涉及的疑似学术不端行为（抄袭、伪造、篡改、重复发表、署名不当等）。其目的在于：  
• 以开放、可验证的方式保存证据，方便校内外独立复核；  
• 借由透明度促进武汉大学改进学术治理；  
• 保护举报人并避免失实指控。  



2. 目录结构  
```
/root
 ├── CODE_OF_CONDUCT.md
 ├── CONTRIBUTING.md
 ├── LICENSE
 ├── README.md               # 强调“仅限武汉大学相关作品”
 └── cases
      └── <DOI>/             # 斜杠 → 下划线
           ├── README.md     # 疑点概述（≤200 字）
           ├── metadata.yaml # 文献信息 + 武大字段
           ├── original/
           ├── analysis/
           └── evidence/
```

3. metadata.yaml 必填字段  
```
doi: 10.1234/abcd.2023.001
title: "论文题目"
authors:
  - 张三
  - 李四
journal: 期刊名称
year: 2023
url: https://doi.org/10.1234/abcd.2023.001
date_added: 2025-08-04
submitter: GitHub用户名
whu_authors:            # 至少一人
  - 张三 (School of Physics and Technology, Wuhan University)
affiliation_proof:      # 例如 PDF 第1页截图或出版社元数据链接
  - evidence/affil_screenshot.png
misconduct_type:        # 选项：plagiarism / fabrication / image_manipulation / duplicate_publication / authorship / other
```

4. 提交流程  
1) Fork → 分支 → 在 `/cases/<DOI>/` 添加文件 → Pull Request。  
2) PR 模板新增武汉大学专用核对框，如果准备合并请先自查：  
   ☐ 该作品作者列表或通讯地址包含“Wuhan University”且已附截图；  
   ☐ 所附材料不侵犯版权或已获许可；  
   ☐ 已对私密信息做匿名化处理。  

5. 证据与分析要求  
• 必须能直接证明作者与武汉大学关联，否则拒绝合并；  
• 其他证据标准同上一版（可验证、完整、可追溯、中立措辞）；  
• 所有比较脚本、图像取证脚本请存于 `analysis/` 并标注运行环境。  

6. 法律与伦理  
• 聚焦行为，不做人身攻击；  
• 遵守《民法典》关于名誉权与信息网络传播权的规定；  
• 如出版社不允许再分发 PDF，则上传 SHA-256 哈希等可以证明唯一性的证据，并提供 DOI 链接。  

7. 行为准则  
参见 `CODE_OF_CONDUCT.md`，重点条款：禁止侮辱、歧视、地域黑；讨论只基于证据与方法。  

8. 免责声明  
仓库维护者与贡献者仅提供材料与分析，未对事实作最终裁断。最终认定应由武汉大学学术道德委员会、期刊编辑部或其他有权机构完成。  

9. 推荐工具
基本上没有什么推荐的方法快速查找到不是那么明显的学术漏洞，还恳请各领域的专家仔细查阅 

11. 许可  
• 仓库文档：CC-BY-4.0；  
• 代码：MIT；  
• 第三方文献遵循原版权。  

（武汉大学疑似学术不端仓库规范完）
