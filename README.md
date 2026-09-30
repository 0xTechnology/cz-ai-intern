# CZ AI 实习生 

<p align="center">
  <img src="./image.jpg" width="200" alt="CZ AI Intern">
</p>

非官方粉丝项目。与 CZ、币安、YZiLabs、BNB Chain 无关。

CA：0xbb8f04649a00d24f187987f1a62e939ea5af7777

CZ 说过：没有实习生帮他管 X 账号。
所以这个实习生只待在 GitHub 上，只在你电脑里写草稿，不会去别人账号发帖。

> 没有实习生管理我的 X 账号。
> 那这名实习生就先住在仓库里。

## 能做什么

- 读一句主题
- 生成一段「实习生口吻」草稿
- 不发推
- 不要 CZ / 币安账号密码

## 怎么运行

```bash
python intern.py "gm"

免责声明恶搞项目，不是投资建议。
禁止冒充 CZ。


4. 拉到页面底部
5. 点 **Commit changes** → 再点确认

---

## 第 4 步：新建 `intern.py`

1. 回到仓库首页
2. 点 **Add file** → **Create new file**
3. 文件名填：`intern.py`
4. 把下面整段贴进去：

```python
#!/usr/bin/env python3
"""本地恶搞实习生。不会发到任何平台。"""

from __future__ import annotations

import argparse
from datetime import datetime, timezone

口吻 = [
    "保持简单。",
    "先把东西做出来。",
    "不构成投资建议。",
    "手打草稿。不会替任何人管账号。",
]


def 写草稿(主题: str) -> str:
    主题 = 主题.strip() or "gm"
    现在 = datetime.now(timezone.utc).strftime("%Y-%m-%d %H:%M UTC")
    return (
        f"[非官方草稿 — 禁止当成 CZ 本人发帖]\n"
        f"时间：{现在}\n"
        f"主题：{主题}\n\n"
        f"gm\n"
        f"{主题}\n"
        f"{口吻[0]}{口吻[1]}\n"
        f"{口吻[2]}\n"
        f"{口吻[3]}\n"
    )


def main() -> None:
    parser = argparse.ArgumentParser(description="CZ AI 实习生本地草稿工具")
    parser.add_argument("主题", nargs="*", help="实习生要写的主题")
    args = parser.parse_args()
    print(写草稿(" ".join(args.主题)))


if __name__ == "__main__":
    main()
