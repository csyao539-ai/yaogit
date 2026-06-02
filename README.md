# yaogit
# admin
# admin

## Nmap 扫描脚本

```bash
#!/bin/bash
# 快速端口扫描脚本

TARGET=$1

if [ -z "$TARGET" ]; then
    echo "用法: ./scan.sh <目标IP或域名>"
    exit 1
fi

echo "=== 正在扫描: $TARGET ==="
echo ""

# 1. 快速扫描常用端口
echo "[1] 扫描常见端口..."
nmap -F "$TARGET"

echo ""
# 2. 服务版本探测
echo "[2] 服务版本探测..."
nmap -sV "$TARGET"

echo ""
# 3. 操作系统探测（需root权限）
echo "[3] 操作系统探测..."
nmap -O "$TARGET" 2>/dev/null || echo "   (需要 root 权限)"

echo ""
echo "=== 扫描完成 ==="
222222222222222222222
```
