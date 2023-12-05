# 資訊安全管理與規劃

# 資訊安全技術與防護

# 資訊安全專業證照
- CISSP
- CEH
- IPAS中階

- # 20230611 期末總成績計算
- 期中考成績: PWN初步測試+Buffer Overflow
  - Buffer Overflow 1: A simple Buffer Overflow attack
  - Buffer Overflow 2: retrun to code | return to text
- 期中平時成績:根據底下錄影挑選二個完成測試報告(PPT)
  - 1.Pwntools實戰PPC 測試報告
    - [SecurityFoscusOnline2023|Python程式與資安應用入門|3.使用Python求解PPC(Professional Program Code)問題](https://github.com/MyFirstSecurity2020/SF2023A3)
    - 教學影片與教材請參考 上述平台
    - 使用平台 == > http://120.114.62.212
    - 至少須完成
      - PPC101::PPC1_hello world 
      - PPC101::PPC2_3rd:pwntools快速入門與示範解題 
      - PPC101::PPC8_temperature
      - PPC101::PPC3_beautify
    - 鼓勵你參看解答完成底下各題
      - PPC101::PPC4_count
      - PPC101::PPC5_lambda
      - PPC101::PPC6_money
      - PPC101::PPC7_calendar
  - 2.Ret2shellcode ATTACK測試報告
    - [程式碼範例](./ret2sc.md) 
    - [PPT](./PPT/2_A888168_11102軟體測試實務_return2sc.pptx)
    - [教學錄影](https://youtu.be/BEtC8hWFbV8)
  - 3.ret2libc ATTACK測試報告
    - [程式碼範例](./ret2libc.md) 
    - [PPT](./PPT/3_A888168_11102軟體測試實務_Ret2libcAttack.pptx)
    - [教學錄影](https://youtu.be/BN2NG3B0RtU)
- 期末考成績:Format strings 漏洞分析報告
    - [程式碼範例](./FormatStrings.md)
    - [PPT](./PPT/5_A888168_11102軟體測試實務_Formatstrings漏洞分析報告.pptx)
    - [教學錄影一: Format strings vulnerability](https://youtu.be/5QD5eMyu4XU)
    - [教學錄影二: Case study: Format strings attack](https://youtu.be/vgGOzZn_8Fw)
    - 額外文件[All You Need to Know About Format String Vulnerabilities](https://www.securecoding.com/blog/format-string-vulnerability/)

# PWN2023

- [課程教材與教學錄影](./課程教材與教學錄影.md)
- [參考資料](./參考資料.md)
- 上課使用的測試環境
- Pwn-CTF   http://120.114.62.210/
  - [參考解答](https://github.com/r888800009/CTF-Solve/tree/master/TAIWANHolyHigh-pwn-ctf)

#  ==> {繳交PPT} | {繳交PPT+OBS}
- 期中考成績: PWN初步測試+Buffer Overflow
  - [教學錄影]
  - [參考資料] 
- 期中平時成績: Ret2shellcode ==> ret2libc
  - 送出兩份攻擊碼 == > pwntools 
  - 攻擊碼1: shellcode
  - 攻擊碼2: Buffer Overflow攻擊
    - 必須知道shellcode 記憶體位址
    - Buffer Overflow ==> 蓋buffer + {return address == shellcode 記憶體位址}
  - level-1.Angelboy_Pwn-2 [上課示範解題]
  - level-2.張元_Pwn-9
- 期末平時成績:Return-oriented programming(ROP)對同學而言太難 ==> 以後再開進階PWN
  - [ROP Emporium](https://ropemporium.com/)
  - [ROP1_rop-emporium-split-64bit](./2023/ROP1.md)
  - [ROP2_rop-emporium-callme-64-bit](./2023/ROP2.md) 
- 期末考成績:Format strings 漏洞分析
  - Format_string_Vulnerability攻擊模式1:
    - 練習題目
      - Level 2/fmtstr
      - Pwn/fmt-1
  - Format_string_Vulnerability攻擊模式2:寫入
    - printf 可以使⽤ %n 來寫入指定的位置
    - 可透過 %c 來指定 %n 要寫入的⼤⼩
    - 練習題目
      - Pwn/fmt-2
      - Pwn/fmt-3
      - Level 1.secret 

