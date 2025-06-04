# 使用官方 Python 镜像作为基础
FROM python:3.12

# 设置环境变量，避免 Python 缓存和乱码
ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1 \
    LANG=C.UTF-8

# 设置工作目录
WORKDIR /app

# 拷贝项目文件
COPY . .

# 安装依赖
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# 暴露端口
EXPOSE 5000

# 启动应用
CMD ["python", "run.py"]
