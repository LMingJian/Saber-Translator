# Saber-Translator

**Saber-Translator** 是一个使用人工智能技术自动翻译日语漫画的工具。 它能够：

*   **自动检测漫画图片中的对话气泡。**
*   **使用 Manga OCR 技术识别气泡中的日语文本。**
*   **利用LLM将日语文本翻译成中文。**
*   **将翻译后的中文文本重新绘制到漫画图片的气泡中。**
*   **提供简洁的 Web 界面，方便上传图片和进行翻译。**

**主要功能:**

*   **单张图片和批量图片翻译:** 支持一次翻译单张漫画图片，也支持上传多张图片进行批量翻译。
*   **可调整的字号大小:** 用户可以自定义翻译后文本的字号大小。
*   **API Key 和模型选择:**  允许用户输入自己的API Key和选择使用的大模型型号。
*   **图片概览和导航:**  提供缩略图侧边栏，方便用户浏览和切换已上传的漫画图片。
*   **翻译结果下载:**  用户可以下载翻译后的漫画图片。

**目前版本支持:**

*   **源语言:** 日语
*   **目标语言:** 简体中文
*   **文本方向:** 竖排从右到左

## 运行环境

*   Python 3.7 或更高版本 (建议使用 Python 3.9+)
*   推荐使用虚拟环境

## 安装步骤

1.  **在Releases下载最新的版本后解压**

2.  **创建虚拟环境:**

        ```bash
        python3 -m venv venv  # macOS/Linux
        python -m venv venv   # Windows
        ```
3.  **激活虚拟环境 :**

    *   **`venv`:**
        *   **macOS/Linux:** `source venv/bin/activate`
        *   **Windows:** `venv\Scripts\activate`

    *   **`conda`:**
        ```bash
        conda activate manga_translator  # 或者你创建的虚拟环境名称
        ```

4.  **安装依赖:**

    ```bash
    pip install -r requirements.txt
    ```

## 使用方法 

1.  **启动程序 :**

    ```bash
    python app.py
    ```

2.  **打开 Web 界面 :**

    程序启动后，会在终端或命令提示符中显示运行地址，通常是 `http://127.0.0.1:5000/`。  打开你的浏览器，访问这个地址。

3.  **使用漫画翻译器:**

    *   **上传图片:**  在网页上，你可以拖拽漫画图片到 "拖拽图片到这里..." 区域，或者点击 "点击选择文件" 链接选择图片文件。 支持单张或多张图片上传。
    *   **设置翻译选项:**  在左侧的 "翻译设置" 侧边栏，你可以设置：
        *   **翻译语言:**  目前默认为 "简体中文"。
        *   **字号大小:**  调整翻译后文本的字号（建议50-60）。
        *   **API Key:**  输入你的API Key。
        *   **模型型号:**  选择要使用的大模型型号 (建议deepseek-ai/DeepSeek-V2.5)。
    *   **翻译图片:**
        *   **翻译当前图片:**  选择缩略图列表中的一张图片，点击 "翻译当前图片" 按钮进行翻译。
        *   **翻译所有图片:**  点击 "翻译所有图片" 按钮，程序将批量翻译所有已上传的图片。
    *   **查看翻译结果:**  翻译完成后，翻译后的图片会显示在 "翻译后图片" 区域。  下方会显示检测到的文本内容。
    *   **图片导航:**  使用 "上一张" 和 "下一张" 按钮切换查看不同的图片。
    *   **下载图片:**  点击 "下载翻译后图片" 按钮下载当前显示的翻译后图片。
    *   **图片概览:**  右侧的 "图片概览" 侧边栏显示已上传图片和翻译后图片的缩略图列表。 点击缩略图可以切换图片。

## 注意事项 

*   **模型文件:**  请务必正确下载和放置 YOLOv5 模型权重文件 (`best.pt`) ，否则程序将无法正常运行。
*   **翻译质量:**  AI 翻译的质量可能受到多种因素影响，例如原文的复杂程度、模型的能力等。  翻译结果可能并非完美，仅供参考。
*   **目前支持:**  当前版本主要针对 **竖排日语漫画** 进行优化。  对其他语言和排版的漫画支持可能有限。

## 未来计划

*   支持更多目标语言 (例如 英语, 繁体中文等)。
*   支持横排文本漫画。
*   优化翻译质量和速度。
*   增加用户自定义字体功能。
*   改进 Web 界面用户体验。

## 贡献

欢迎任何形式的贡献，包括但不限于：

*   代码改进和 Bug 修复。
*   新功能开发。
*   文档完善。
*   问题反馈和建议。

如果你想为本项目贡献代码，请 Fork 本仓库，进行修改后提交 Pull Request。

**感谢使用 AI 漫画翻译器!  希望这个工具能帮助你更好地阅读和理解日语漫画。** 😊

