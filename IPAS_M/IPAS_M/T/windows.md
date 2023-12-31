### 更多 windows 指令(有時間請多多充實windows 指令的用法)
- [netstat](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/netstat) |  [中文版](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/netstat)
  - 顯示作用中的 TCP 連線、電腦正在接聽的埠、乙太網路統計資料、IP 路由表、IP 路由表、IP IP 流量統計資料 (、ICMP、TCP 和 UDP 通訊協定) ，以及 IPv6、ICMPv6、透過 IPv6 的 TCP，以及透過 IPv6 通訊協定的 UDP) 的 IPv6 統計資料 (。 不使用參數，此命令會顯示作用中的 TCP 連線。
  - `-a`	==> 顯示電腦正在接聽的所有作用中 TCP 連線和 TCP 和 UDP 埠。
  - `-n`	==> 僅顯示作用中的 TCP 連線 ==> 位址和埠號碼會以數值表示，不會嘗試做名稱解析
  - `-o` ==> 顯示作用中的 TCP 連線，並包含每個連線 (PID) 的進程識別碼。 您可以在 Windows 工作管理員的 [進程] 索引標籤上，根據 PID 找到應用程式。
  - 試試看: netstat -ano 和 netstat -an 有何差別?
- [netsh](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/netsh)  | [中文版](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/netsh)
  - 網路殼層命令列腳本公用程式，可讓您在本機或遠端顯示或修改目前執行中電腦的網路組態。
  - netsh /? ==> 
- [nbtstat](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/nbtstat) | [中文版](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/nbtstat)
  - 顯示 NetBIOS over TCP/IP (NetBT) 通訊協定統計資料、本機電腦和遠端電腦的 NetBIOS 名稱資料表，以及 NetBIOS 名稱快取。
  - 此命令也允許重新整理 NetBIOS 名稱快取，以及向 Windows 網際網路名稱服務註冊的名稱， (WINS) 。 不使用參數，此命令會顯示 [說明] 資訊。 
- [auditpol](https://learn.microsoft.com/zh-tw/windows-server/administration/windows-commands/auditpol)  ==> audit policy |顯示和 執行函式以操作`稽核原則(audit policies)`的相關資訊
  - Displays information about and performs functions to manipulate audit policies
  - 功能:
    - 設定和查詢系統稽核原則。
    - 設定和查詢個別使用者稽核原則。
    - 設定和查詢稽核選項。
    - 設定和查詢用來委派稽核原則存取權的安全性描述項。
    - (CSV) 文字檔，將稽核原則報告或備份至逗號分隔值。
    - 從 CSV 文字檔載入稽核原則。
    - 設定全域資源 SCL。
  - 指令參數
    - /get	==> 顯示目前的稽核原則。 
    - /set	==>設定稽核原則。
    - /list	==>顯示可選取的原則元素。 
    - /backup ==>將稽核原則儲存至檔案。
    - /restore	==>從先前使用 auditpol /backup 建立的檔案還原稽核原則。
    - /clear	==>清除稽核原則。
    - /remove	==>移除所有使用者稽核原則設定，並停用所有系統稽核原則設定。
    - /resourceSACL	==>設定全域資源系統存取控制清單， (SCL) 。 注意： 僅適用于 Windows 7 和 Windows Server 2008 R2。
    - /?	==>在命令提示字元顯示說明。 
  - 範例:
    - auditpol /set `/user:mikedan` `/category:detailed Tracking` `/include /success:enable`
      - 針對使用者 mikedan 的詳細追蹤類別下的所有子類別設定每個使用者稽核原則，以便稽核所有使用者的成功嘗試
    - auditpol /set /category:detailed Tracking /success:enable
      - 對詳細追蹤類別下的所有子類別設定系統稽核原則，以只包含成功嘗試的稽核
- BOOTCFG ==> Configures, queries, or changes Boot.ini file settings.
  - 用來設定、查詢、變更或刪除 BOOT.INI 檔案中的開機項目設定
  - `BOOTCFG /parameter [arguments]`
## wmic
- 範例
  - wmic context ==> 顯示所有全域參數的目前值

## Wiondows 強大的PowerShell
- Windows 有兩種cocmmand shell
  - cmd  ==> 啟動一個 Windows 命令直譯器的新instance
  - powershell
- Windows PowerShell是以工作為基礎的命令列殼層和指令碼語言，專為系統管理而設計。
- Windows PowerShell 是以 .NET Framework 為基礎所建置
- PowerShell協助 IT 專業人員與進階使用者控制和自動化管理 Windows 作業系統與在 Windows 上執行的應用程式 

## Windows 系統資訊 ==> registry
- 系統資訊
  - 控制碼和物件==>	物件是代表系統資源的資料結構，例如檔案、執行緒或圖形影像。 應用程式無法直接存取物件資料或物件所代表的系統資源。 相反地，應用程式必須取得物件
  - 控制碼，以便用來檢查或修改系統資源。
  - [登錄registry](https://learn.microsoft.com/zh-tw/windows/win32/sysinfo/registry) ==>	系統定義的資料庫，應用程式和系統會儲存和擷取組態資訊。
    - [中文版]()
    - 登錄是系統定義的資料庫
    - 應用程式和系統元件會儲存和擷取組態資料。
    - 儲存在登錄中的資料會根據 Microsoft Windows 的版本而有所不同。
    - 應用程式會使用登錄 API 來擷取、修改或刪除登錄資料。
    - 除非絕對必要，否則您不應該編輯不屬於應用程式的登錄資料。
    - 如果登錄中有錯誤，您的系統可能無法正常運作。
    - 如果發生這種情況，您可以將登錄還原到上次成功啟動電腦時的狀態。 
  - 系統資訊	擷取或設定系統組態、設定、版本和計量。
  - Time	擷取或設定系統時間。
  - 時間提供者	從硬體或網路擷取精確的時間戳記，並提供時間戳記給網路上的其他用戶端。
  - [WaaS 評定平臺(Windows as a Service (WaaS) update evaluation platform)]() | [中文版](https://learn.microsoft.com/zh-tw/windows/win32/sysinfo/about-update-assessor-service)
