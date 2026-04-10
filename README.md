# pdf_to_long_image_optimized
PDF 转长图工具 
中文版本
📄 PDF 转长图工具
一个简单易用的 PDF 转长图工具，支持自动裁剪白边、去除重复页眉、自定义边框等功能。适用于将多页 PDF 文档转换为一张无缝衔接的长图。

✨ 功能特点
✅ 自动裁剪留白 - 智能识别并裁剪每页四周的白色边距

✅ 去除重复标题 - 除第一页外，可额外裁剪顶部区域（去除重复的页眉/标题）

✅ 无缝拼接 - 将多页内容垂直拼接成一张完整长图

✅ 自定义边框 - 最后可为整张图片添加白色边框，美观大方

✅ 可调节清晰度 - 支持 DPI 参数调节，平衡清晰度和文件大小

✅ 简单易用 - 只需将 PDF 文件放入目录，运行脚本即可

📦 安装依赖
bash
pip install pdf2image pillow
额外依赖（Windows 用户）
需要安装 poppler 才能使用 pdf2image：

下载 poppler

解压到 D:\poppler（或其他目录）

在代码中指定路径，或添加到系统 PATH

🚀 快速开始
将 PDF 文件放入项目目录，命名为 指定文件名.pdf
如果是word文档，请将文件转换为pdf（另存为pdf）

运行脚本：

bash
python pdf_to_long_image_optimized.py
在相同目录下找到生成的 PNG 图片

⚙️ 配置参数
参数	说明	默认值
dpi	输出清晰度	200
crop_tolerance	白边裁剪容忍度（越大越激进）	15
border	最终白边框宽度（像素）	50
extra_top_crop	非第一页额外裁剪顶部像素	100
📁 项目结构
text
PDFtoIMG/
├── pdf_to_long_image_optimized.py   # 主程序
├── 指定文件名.pdf               # 输入的 PDF 文件
└── 指定文件名_YYYYMMDD.png     # 输出的长图
📝 使用示例
python
pdf_to_long_image_clean(
    pdf_file, 
    output_file,
    dpi=200,              # 清晰度
    crop_tolerance=15,    # 留白裁剪容忍度
    border=50,            # 白边框宽度
    extra_top_crop=100    # 第二页起裁剪顶部
)
❓ 常见问题
Q: 生成的图片太大怎么办？
A: 降低 dpi 参数（如 150），或减小 border 值。

Q: 裁剪太激进，内容被裁掉了？
A: 减小 crop_tolerance（如改为 10）。

Q: 第二页的标题没有被完全去除？
A: 增大 extra_top_crop 值（如改为 120 或 150）。

Q: 报错 poppler not found？
A: 请正确安装 poppler 并在代码中指定路径。

📄 许可证
MIT License

English Version
📄 PDF to Long Image Tool
A simple and easy-to-use tool that converts PDF documents into seamless long images. Supports automatic whitespace cropping, duplicate header removal, and custom borders.

✨ Features
✅ Auto Crop Whitespace - Intelligently identifies and removes white margins around each page

✅ Remove Duplicate Headers - Extra top cropping for pages after the first (removes repeated headers/titles)

✅ Seamless Stitching - Vertically stitches multiple pages into one continuous long image

✅ Custom Border - Adds a white border around the final image for a polished look

✅ Adjustable Quality - DPI parameter for balancing clarity and file size

✅ Easy to Use - Simply place your PDF file in the directory and run the script

📦 Installation
bash
pip install pdf2image pillow
Additional Dependency (Windows Users)
poppler is required for pdf2image:

Download poppler

Extract to D:\poppler (or any directory)

Specify the path in the code or add to system PATH

🚀 Quick Start
Place your PDF file in the project directory and name it fileName.pdf

Run the script:

bash
python pdf_to_long_image_optimized.py
Find the generated PNG image in the same directory

⚙️ Configuration Parameters
Parameter	Description	Default
dpi	Output quality	200
crop_tolerance	Whitespace cropping aggressiveness (higher = more aggressive)	15
border	Final white border width (pixels)	50
extra_top_crop	Extra top cropping for pages after the first	100
📁 Project Structure
text
PDFtoIMG/
├── pdf_to_long_image_optimized.py   # Main script
├── fileName.pdf               # Input PDF file
└── fileName_YYYYMMDD.png     # Output long image
📝 Usage Example
python
pdf_to_long_image_clean(
    pdf_file, 
    output_file,
    dpi=200,              # Quality
    crop_tolerance=15,    # Whitespace cropping tolerance
    border=50,            # White border width
    extra_top_crop=100    # Extra top crop for pages after first
)
❓ FAQ
Q: The generated image is too large?
A: Reduce the dpi parameter (e.g., to 150) or decrease the border value.

Q: Content is being cropped out?
A: Decrease crop_tolerance (e.g., to 10).

Q: The header on the second page isn't fully removed?
A: Increase the extra_top_crop value (e.g., to 120 or 150).

Q: Error: poppler not found?
A: Install poppler correctly and specify the path in the code.

📄 License
MIT License

🤝 Contributing
Issues and pull requests are welcome!

📧 Contact
For questions or suggestions, please open an issue on GitHub.

