# 2FA Bypass Techniques(2FA 绕过技术)

### [Mindmap](https://mm.tt/1736437018?t=SEeZOmvt01)

Index | Technique
--- | ---
**1** | Response Manipulation(响应操纵)
**2** | Status Code Manipulation(状态码操作)
**3** | 2FA Code Leakage in Response(2FA代码泄漏响应)
**4** | JS File Analysis(JS文件分析)
**5** | 2FA Code Reusability(2FA 代码可重用性)
**6** | Lack of Brute-Force Protection(缺乏蛮力保护)
**7** | Missing 2FA Code Integrity Validation(缺少 2FA 代码完整性验证)
**8** | CSRF on 2FA Disabling(CSRF 关于 2FA 禁用)
**9** | Password Reset Disable 2FA(密码重置禁用 2FA)
**10** | Backup Code Abuse(备份代码滥用)
**11** | Clickjacking on 2FA Disabling Page(点击劫持 2FA 禁用页面)
**12** | Enabling 2FA doesn't expire Previously active Sessions(启用 2FA 不会过期)
**13** | Bypass 2FA with null or 000000(使用 null 或 000000 绕过 2FA)
___
#### Response Manipulation - 响应操纵
```
In response if "success":false
Change it to "success":true
```

#### Status Code Manipulation - 状态码操作

```
If Status Code is 4xx
Try to change it to 200 OK and see if it bypass restrictions
```
#### 2FA Code Leakage in Response - 2FA代码泄漏响应
```
Check the response of the 2FA Code Triggering Request to see if the code is leaked.
```
#### JS File Analysis - JS文件分析
```
Rare but some JS Files may contain info about the 2FA Code, worth giving a shot
```
#### 2FA Code Reusability - 2FA 代码可重用性
```
Same code can be reused
```
### Lack of Brute-Force Protection 缺乏蛮力保护
```
Possible to brute-force any length 2FA Code
```
#### Missing 2FA Code Integrity Validation - 缺少 2FA 代码完整性验证
```
Code for any user acc can be used to bypass the 2FA
```
#### CSRF on 2FA Disabling
```
No CSRF Protection on disabling 2FA, also there is no auth confirmation
```
#### Password Reset Disable 2FA - 密码重置禁用 2FA
```
2FA gets disabled on password change/email change
```
#### Backup Code Abuse - 备份代码滥用
```
Bypassing 2FA by abusing the Backup code feature
Use the above mentioned techniques to bypass Backup Code to remove/reset 2FA restrictions
```
#### Clickjacking on 2FA Disabling Page - 点击劫持 2FA 禁用页面
```
Iframing the 2FA Disabling page and social engineering victim to disable the 2FA
```
#### Enabling 2FA doesn't expire Previously active Sessions - 启用 2FA 不会过期
```
If the session is already hijacked and there is a session timeout vuln
```
#### Bypass 2FA with null or 000000
```
Enter the code 000000 or null to bypass 2FA protection.
```
