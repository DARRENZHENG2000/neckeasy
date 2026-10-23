# NeckEasy 颈逸 · 交互介绍页

阿波罗镜片专业事务部内部资料。页面经 StaticCrypt（AES-256，PBKDF2 派生密钥）加密，仓库中只有密文；访问需输入密码。

- 在线地址：GitHub Pages（见仓库 About）
- 更新方式：由专业事务部在本地明文源文件上修改后重新加密，覆盖 `index.html` 推送即可。`.staticrypt.json` 中的 salt 保持不变，同事浏览器中的“记住我”在更新后仍然有效。

```bash
npx staticrypt@3 NeckEasy_src.html -p '<密码>' --short --remember 30 -d out   # 读取同目录 .staticrypt.json 的 salt
mv out/NeckEasy_src.html index.html
```
