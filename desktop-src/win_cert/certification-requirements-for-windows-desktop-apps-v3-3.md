---
title: " (v3) 的桌面認證需求"
description: 檔3.3 年3月18日，2014This 檔包含傳統型應用程式必須滿足的技術需求和資格資格，才能參與 Windows 8.1 的桌面應用程式認證計畫。
ms.assetid: BD4765EA-C8A1-4A9F-9C50-479A3612DB85
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb2bbcff3e3b00235c88ebc470c1a45e5063f1d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879697"
---
# <a name="certification-requirements-for-windows-desktop-apps-v33"></a>Windows 傳統型應用程式的認證需求3.3 版

**檔版本：** 3。3

**檔日期：** 2014年3月18日

本檔包含傳統型應用程式必須滿足的技術需求和資格資格，才能參與 Windows 8.1 的桌面應用程式認證計畫。 針對 Windows 7，此程式稱為 Windows 軟體標誌計畫。

## <a name="welcome"></a>歡迎！

Windows 平臺支援廣泛的產品和合作夥伴生態系統。 在您的產品上顯示 Windows 標誌代表 Microsoft 與貴公司之間的關聯性和品質共同承諾。 客戶信任您產品上的 Windows 品牌，因為它可確保其符合相容性標準，並在 Windows 平臺上順利執行。 成功傳遞 Windows 應用程式認證可讓您的應用程式在 Windows 相容性中心內展示，同時也是在 Windows 存放區中列出傳統型應用程式參考的必要步驟。

Windows 的應用程式認證計畫是由程式和技術需求所組成，可協助確保攜帶 Windows 品牌的協力廠商應用程式，在執行 Windows 的電腦上很容易安裝及可靠。 客戶在購買的系統中有價值的穩定性、相容性、可靠性、效能和品質。 Microsoft 致力於滿足這些軟體應用程式的需求，這些需求是設計在電腦的 Windows 平臺上執行。 這些工作包括在執行 Windows 軟體的電腦上，效能一致性、改善效能和增強安全性的相容性測試。 Microsoft 相容性測試是與業界合作夥伴合作設計，並且持續改進以回應產業開發和消費者需求。

Windows 應用程式認證套件用來驗證這些需求是否符合規範，並取代 Windows 7 軟體標誌計畫中用於驗證的 WSLK。 Windows 應用程式認證套件是 Windows 軟體開發套件 (SDK) 中包含的其中一個元件，適用于 Windows 8.1。

## <a name="app-eligibility"></a>應用程式資格

若要讓應用程式符合 Windows 8.1 傳統型應用程式認證的資格，則必須符合下列準則和本檔中所列的所有技術需求。

-   它必須是獨立應用程式
-   它必須在本機 Windows 8.1 電腦上執行
-   它可以是認證 Windows Server 應用程式的用戶端元件
-   它必須是程式碼並已完成功能
-   它不能透過本機機制與 Windows 存放區應用程式進行通訊，包括透過檔案和登錄機碼，但支援的企業案例除外
-   它不得危及或危及 Windows 系統的安全性或功能
-   它必須有唯一的名稱，而且不得由其他人商標
-   所有外部元件都必須分開認證或符合 Windows 應用程式認證套件
-   針對任何配套的應用程式，它必須有退出選項

如果桌面應用程式提交到防毒軟體及/或防間諜軟體 (也就是反惡意程式碼) products 類別，則必須遵守反惡意程式碼平臺的指導方針。 WINDOWS 8 反惡意程式碼 API 授權合約必須已簽署並在提交前生效。 夥伴必須是的成員，或讓研究人員必須是的成員，而且在合約中列出的組織中也是如此。 這項功能必須透過合約中列出的組織 Windows 8 認證。 在過去12個月內，應用程式必須至少經過測試一次，並通過偵測和清除的認證。

## <a name="1-apps-are-compatible-and-resilient"></a>1. 應用程式相容且具有復原能力

應用程式損毀或停止回應的時間會導致使用者挫折。 應用程式應該具有復原能力和穩定性，並消除這類失敗有助於確保軟體的可預測性、可維護性、效能和值得信賴。<dl> 1.1 您的應用程式不得相依于 Windows 相容性模式、AppHelp 訊息和或任何其他相容性修正程式  
1.2 您的應用程式必須有相容性資訊清單，並針對支援的版本使用適當的 Guid Windows  
1.3 您的應用程式必須是 DPI 感知，方法是使用應用程式的組件資訊清單，而不是呼叫 SetProcessDPIAware  
1.4 您的應用程式不得依賴 VB6 執行時間  
1.5 您的應用程式不能載入任意 dll 來攔截 WIN32 API 呼叫，請使用 HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows AppInit \_ dll。  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. 應用程式必須遵守 Windows 安全性最佳作法

使用 Windows 的安全性最佳作法有助於避免暴露于 Windows 攻擊面。 攻擊面是惡意攻擊者利用目標軟體中的弱點來惡意探索作業系統的進入點。 其中一個最糟的安全性弱點是權限提高。

<dl> 2.1 您的應用程式必須使用強式和適當的 <a href="/windows/desktop/SecAuthZ/access-control-lists">acl</a> 來保護可執行檔  
2.2 您的應用程式必須使用強式和適當的 <a href="/windows/desktop/SecAuthZ/access-control-lists">acl</a> 來保護目錄的安全  
2.3 您的應用程式必須使用強式和適當的 <a href="/windows/desktop/SecAuthZ/access-control-lists">acl</a> 來保護登錄機碼  
2.4 您的應用程式必須使用強式和適當的 <a href="/windows/desktop/SecAuthZ/access-control-lists">acl</a> 來保護包含物件的目錄  
2.5 您的應用程式必須將非系統管理員存取權減少到易受到篡改的服務  
2.6 您的應用程式必須防止具有快速重新開機的服務，每24小時重新開機超過兩次
</dl><strong>注意：只能將存取權授與需要它的實體。</strong>

Windows 的應用程式認證計畫會確認 acl 和服務是否以不會造成 Windows 系統風險的方式來執行，藉此驗證是否未公開 Windows 攻擊面。

## <a name="3-apps-support-windows-security-features"></a>3. 應用程式支援 Windows 安全性功能

Windows 作業系統有許多支援系統安全性和隱私權的功能。 應用程式必須支援這些功能，才能維持作業系統的完整性。 編譯不當的應用程式可能會造成緩衝區溢位，進而導致拒絕服務或允許惡意程式碼執行。 <dl> 3.1 您的應用程式不能使用 AllowPartiallyTrustedCallersAttribute (APTCA) 來確保安全地存取強式名稱的元件  
3.2 您的應用程式必須使用/SafeSEH 旗標進行編譯，以確保安全的例外狀況處理  
3.3 您的應用程式必須使用/NXCOMPAT 旗標進行編譯，以防止資料執行  
3.4 您的應用程式必須使用/DYNAMICBASE 旗標（位址空間配置隨機載入 (ASLR）進行編譯)   
3.5 您的應用程式不得讀取/寫入共用的 PE 區段  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. 應用程式必須遵守系統重新開機管理員訊息

當使用者啟動關機時，通常會有強烈的願望可以看到關機成功;他們可能會在離開辦公室的同時，只想要讓電腦關閉。 應用程式必須遵守此需求，而不會封鎖關機。 雖然在大部分情況下，關閉可能不會很重要，但應用程式必須針對重大關機的可能性做好準備。<dl> 4.1 您的應用程式必須適當地處理重大關機 <dl> 在重大關機中，傳回 FALSE 到 WM QUERYENDSESSION 的應用程式 \_ 將會傳送至 wm \_ ENDSESSION 且已關閉，而這些應用程式將會 \_ 被終止。  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> \_具有 LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 的 WM QUERYENDSESSION。  
主控台應用程式可以呼叫 SetConsoleCtrlHandler 來指定將處理關機通知的函數。 服務應用程式可以呼叫 RegisterServiceCtrlHandlerEx 來指定將會接收關機通知的函數。  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> \_具有 LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 的 WM ENDSESSION。  
應用程式至少應儲存任何使用者資料，並在重新開機之後指出所需的資訊，來做好準備。  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl><strong>注意：因為無法中斷的作業而必須封鎖關機的應用程式應該會解釋使用者的原因。</strong> 使用 ShutdownBlockReasonCreate 來註冊說明使用者原因的字串。 當作業完成時，應用程式應該呼叫 ShutdownBlockReasonDestroy 來指示系統可以關機。

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. 應用程式必須支援乾淨且可還原的安裝

乾淨、可還原的安裝可讓使用者順利管理 (在其系統上部署和移除) 應用程式。<dl> 5.1 您的應用程式必須正確地執行乾淨且可還原的安裝 <dl> 如果安裝失敗，應用程式應該要能夠回復，並將機器還原成先前的狀態。  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> 在安裝、卸載或更新結束時，重新開機電腦絕對不應該是唯一的選項。 使用者應該有機會稍後重新開機。  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Windows 清查工具和遙測工具需要已安裝應用程式的完整資訊。 如果您使用以 MSI 為基礎的安裝程式，MSI 會自動建立下面的登錄專案。 如果您不是使用 MSI 安裝程式，則安裝模組必須在安裝期間建立下列登錄專案：  
</dl>

-   DisplayName
-   InstallLocation
-   Publisher
-   UninstallString
-   VersionMajor 或 MajorVersion
-   VersionMinor 或 MinorVersion

</dd> 5.6 The app must remove all of its entries from Add/ Remove Programs upon uninstall  
</dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. 應用程式必須數位簽署檔案和驅動程式

Authenticode 數位簽章可讓使用者確認軟體是否為正版。 它也可讓您偵測檔案是否已遭篡改，例如是否受病毒感染。 核心模式程式碼簽署強制是一項稱為程式碼完整性 (CI) 的 Windows 功能，可在每次將檔案映射載入記憶體時驗證檔案的完整性，藉此改善作業系統的安全性。 CI 會偵測惡意程式碼是否已修改系統二進位檔案。 當核心模組的簽章無法正確確認時，也會產生診斷和系統審核記錄事件。 <dl> 6.1 所有可執行檔 (.exe、.dll、.ocx、.sys、.cpl、winspool.drv、scr) 都必須使用 Authenticode 憑證進行簽署  
6.2 應用程式安裝的所有核心模式驅動程式都必須具備透過 Windows 硬體認證計畫取得的 Microsoft 簽名。 所有檔案系統篩選器驅動程式都必須由 Microsoft 簽署。  
6.3 例外狀況和豁免 <dl> 只有未簽署的協力廠商可轉散發套件（不含驅動程式）才會考慮豁免。 若要授與此棄權的要求，必須對要求籤署版本的可轉散發套件 () s 進行通訊證明。  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. 應用程式不會根據作業系統版本檢查封鎖安裝或應用程式啟動

當客戶沒有技術限制時，請務必讓客戶無法安裝或執行其應用程式。 一般來說，如果應用程式是針對 Windows Vista 或更新版本的 Windows 所撰寫，則應該不需要檢查作業系統版本。<dl> 7.1 您的應用程式不能執行版本檢查是否相等 <dl> 如果您需要特定功能，請檢查功能本身是否可用。 如果您需要 Windows xp，請檢查 Windows XP 或更新版本 (>= 5.1) 。 如此一來，您的偵測程式碼將繼續在未來的 Windows 版本上運作。 驅動程式安裝程式和卸載模組絕對不應該檢查作業系統版本。  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   以一個套件的形式傳遞的應用程式也會在 Windows XP、Windows Vista 和 Windows 7 上執行，並且需要檢查作業系統版本，以判斷要在指定的作業系統上安裝哪些元件。
-   只會在安裝期間檢查作業系統的最小版本 (的應用程式，而不是只使用核准的 API 呼叫在執行時間) ，而且會正確地列出應用程式資訊清單中的最低版本需求。
-   安全性應用程式 (防毒軟體、防火牆等 ) 、系統公用程式 (例如，使用已核准的 API 呼叫檢查作業系統版本的磁碟重組、備份及診斷工具) 。


</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. 應用程式不會以安全模式載入服務或驅動程式

保管庫模式可讓使用者診斷 Windows 並進行疑難排解。 驅動程式和服務不可設定為以安全模式載入，除非基本系統作業需要這些驅動程式和服務，例如存放裝置磁碟機或診斷和復原用途，例如防病毒掃描程式。 根據預設，當 Windows 處於安全模式時，只會啟動隨 Windows 預先安裝的驅動程式和服務。

-   8.1 例外狀況和豁免 <dl> 必須以安全模式啟動的驅動程式和服務需要棄權。 棄權要求必須包含每個適用的驅動程式或寫入安全開機登錄機碼的服務，並描述應用程式或服務必須在安全模式中執行的技術原因。 應用程式安裝程式必須使用下列登錄機碼註冊所有這類驅動程式和服務：  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

<strong>注意：</strong> 您必須測試這些驅動程式和服務，以確保它們在安全模式下運作，而不會發生任何錯誤。

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. 應用程式必須遵循使用者帳戶控制指導方針

某些 Windows 的應用程式會在系統管理員帳戶的安全性內容中執行，而應用程式通常會要求過多的使用者權限和 Windows 許可權。 控制對資源的存取可讓使用者控制其系統，並防止不必要的變更。 不必要的變更可能是惡意的，例如控制電腦的 rootkit，或是由許可權有限的人員所做的動作結果。 控制資源存取最重要的規則就是提供使用者執行其必要工作所需的最少量存取標準使用者內容。 遵循使用者帳戶控制 (UAC) 指導方針會在應用程式需要應用程式時，為應用程式提供必要的許可權，而不會讓系統持續暴露于安全性風險。 大部分的應用程式在執行時間並不需要系統管理員許可權，而且應該是以標準使用者身分執行。<dl> 9.1 您的應用程式必須有定義執行層級的資訊清單，並告知操作系統應用程式需要哪些許可權才能執行 <dl> 應用程式資訊清單標記僅適用于 Exe （而不是 Dll）。 這是因為在處理常式建立期間，UAC 並不會檢查 Dll。 另外值得注意的是，UAC 規則並不適用于 Microsoft 服務。 資訊清單可以是內嵌或外部。  
若要建立資訊清單，請建立名為 <應用程式 \_ 名稱 # C1.exe 的檔案，並將它儲存在與 EXE 相同的目錄中。 請注意，如果應用程式具有內部資訊清單，則會忽略任何外部資訊清單。 例如：  
<並無 requestedexecutionlevel level = "" asInvoker \| highestAvailable \| requireAdministrator "" uiAccess = "" true \| false ""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> 任何系統管理功能都必須移至以系統管理許可權執行的個別進程。 使用者面向的應用程式，例如可透過 [開始] 功能表上的程式群組存取的應用程式，以及需要提高許可權的應用程式，都必須經過 Authenticode 簽署。  
</dl> </dd> 9.3 Exceptions and Waivers <dl> 以更高的許可權執行其主要進程的應用程式需要棄權 (requireAdministrator 或 highestAvailable) 。 主要進程會識別為應用程式的使用者進入點。 在下列案例中，將會考慮棄權：

-   執行層級設為 highestAvailable 和/或 requireAdministrator 的系統管理或系統工具
-   只有協助工具或 UI 自動化架構應用程式會將 uiAccess 旗標設為 true，以略過使用者介面許可權隔離 (UIPI) 。 若要適當地開始使用應用程式，此旗標必須經過 Authenticode 簽署，而且必須位於檔案系統中受保護的位置，也就是 Program Files。


</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. 根據預設，應用程式必須安裝到正確的資料夾

使用者的預設安裝位置應該具有一致且安全的體驗，同時維持在其選擇的位置安裝應用程式的選項。 此外，您也必須將應用程式資料儲存在正確的位置，以允許多人使用同一部電腦，而不會損毀或覆寫彼此的資料和設定。 Windows 提供檔案系統中的特定位置，以儲存程式和軟體元件、共用應用程式資料，以及使用者專屬的應用程式資料<dl> 10.1 您的應用程式預設必須安裝在 Program Files 資料夾中 <dl> 適用于% ProgramFiles% 中的原生32位和64位應用程式，以及在 x64 上執行32位應用程式的% ProgramFiles (x86) %。 因為此資料夾所設定的安全性許可權，所以使用者資料或應用程式資料永遠不會儲存在此位置。  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> 例如，您的應用程式不應設定下列任何一項;  
</dl>

-   登錄執行金鑰 HKLM、或軟體 \\ Microsoft \\ Windows \\ CurrentVersion 下的 HKCU
-   登錄執行金鑰 HKLM 和或 HKCU 下的 Software \\ Wow6432Node \\ Microsoft \\ windows \\ CurrentVersion
-   開始功能表 AllPrograms > 啟動

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\&lt;username&gt;\\AppData  
10.5 Your app must never write directly to the "Windows" directory and or subdirectories <dl> 使用正確的方法來安裝檔案，例如字型或驅動程式。  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> 當應用程式安裝完成時，將不會有正確的使用者位置來儲存資料。 在安裝之後，應用程式嘗試修改電腦層級的預設關聯線為將會失敗。 相反地，預設值必須在每個使用者層級宣告，如此可防止多個使用者覆寫彼此的預設值。  
</dl> </dd> 10.7 Exceptions and Waivers <dl> 寫入全域組件快取 (GAC 的應用程式必須要有棄權) .NET 應用程式應該將元件相依性保留為私用，並將其儲存在應用程式目錄中，除非明確需要共用元件。  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. 應用程式必須支援多個使用者會話

Windows 的使用者應該能夠在不發生衝突或中斷的情況下執行並行會話。<dl> 11.1 您的應用程式必須確保在本機或遠端執行多個會話時，應用程式的一般功能不會受到負面影響  
11.2 您的應用程式設定和資料檔案不能跨使用者保存  
11.3 使用者的隱私權和喜好設定必須與使用者會話隔離  
11.4 您的應用程式實例必須彼此隔離 <dl> 這表示應用程式的另一個實例看不到來自某個實例的使用者資料。 非作用中使用者會話中的音效不應該在使用中的使用者會話中聽到。 在多個應用程式實例使用共用資源的情況下，應用程式必須確保不會發生衝突。  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> 請參閱 UAC 需求。  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl><strong>注意： </strong> 如果應用程式不支援多個使用者會話或遠端存取，從這類會話啟動時，它必須明確陳述這一點。

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. 應用程式必須支援 x64 版本的 Windows

當64位硬體變得更常見時，使用者會期望應用程式開發人員將其應用程式遷移至64位，或應用程式的32位版本在 Windows 的64位版本下正常執行，以利用64位架構的優點。<dl> 12.1 您的應用程式必須以原生方式支援64位，或者，至少32位 Windows 架構的應用程式必須在64位系統上順暢地執行，才能維持與64位版本的相容性 Windows  
12.2 您的應用程式及其安裝程式不得包含任何16位程式碼，或依賴任何16位元件  
12.3 您的應用程式安裝程式必須偵測並安裝適用于64位架構的適當驅動程式和元件  
12.4 任何 shell 外掛程式都必須在64位版本的 Windows 上執行  
在 WoW64 模擬器下執行的12.5 應用程式不應嘗試破壞或略過 Wow64 虛擬化機制 <dl> 如果有特定案例，應用程式必須偵測它們是否正在 WoW64 模擬器下執行，則應該呼叫 IsWow64Process 來執行此動作。  
</dl> </dd> </dl>

## <a name="conclusion"></a>結論

當這些需求演進時，我們會注意以下修訂歷程記錄中的變更。 穩定的需求是執行最佳工作的關鍵，因此我們的目標是要確保我們所做的變更具有持續性，並持續保護和強化您的應用程式。

再次感謝您參與我們的承諾，以提供絕佳的客戶體驗。

## <a name="revision-history"></a>修訂歷程記錄



| 日期         | 版本 | 修訂描述                   | 文件連結                                                             |
|--------------|---------|----------------------------------------|------------------------------------------------------------------------------|
| 2011年12月20日 | 1.0     | 預覽的檔初稿。 |                                                                              |
| 2012年1月26日 | 1.1     | 更新為第 \# 2 節。                 | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md) |
| 2012年5月31日 | 1.2     | 已新增摘要測試結果             | [1.2](archive--certification-requirements-for-windows-desktop-apps-v1-2.md) |
| 2012年6月29日 | 3.0     | Windows 8 最終檔               | [3.0](archive--certification-requirements-for-windows-desktop-apps-v3-0.md) |
| 2013年6月18日 | 3.1     | Windows 8.1 檔                   | [3.1](archive--certification-requirements-for-windows-desktop-apps-v3-1.md) |
| 2014年2月20日 | 3.2     | 內部更新                        |                                                                              |
| 2014年3月18日 | 3.3     | Windows 8.1 更新版1                   | 3.3                                                                          |





## <a name="learn-more-about-desktop-app-certification"></a>深入瞭解傳統型應用程式認證



| 需求                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 其他詳細資訊                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 相容性與復原能力                                                    | 當機 & 當機時，會導致使用者嚴重中斷，並導致挫折。 應用程式應該具有復原能力和穩定性，消除這類失敗有助於確保軟體的可預測性、可維護性、效能和可信度。<br/> 使用者面向的應用程式進入點必須針對相容性進行資訊清單，以及宣告正確的 GUID。<br/> 使用者面向的應用程式進入點必須針對高 DPI 感知來提供，而且會呼叫適當的 Api 來支援高 DPI。<br/>                                                                                                                                                                                                                                                                                                       | [WindowsVista、Windows 7 和 Windows 8 作業系統](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [應用程式驗證器](/previous-versions/aa480483(v=msdn.10))<br/> [AppInit Dll](https://support.microsoft.com/kb/197571)<br/> [應用程式 (可執行檔) 資訊清單](/windows/desktop/w8cookbook/application--executable--manifest)<br/> [撰寫高 DPI 的 Win32 應用程式](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))<br/> |
| 遵循 Windows 安全性的最佳作法                                       | 使用 Windows 的安全性最佳作法有助於避免暴露于 Windows 攻擊面。 攻擊面是惡意攻擊者利用目標軟體中的弱點來惡意探索作業系統的進入點。 其中一個最糟的安全性弱點是權限提高。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Attack Surface Analyzer](https://technet.microsoft.com/security/gg749821)<br/> [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 支援 Windows 安全性功能                                               | Windows 作業系統已實行許多量值，以支援系統安全性和隱私權。 應用程式必須支援這些措施，才能維持作業系統的完整性。 編譯不當的應用程式可能會導致緩衝區溢位，進而導致拒絕服務或執行惡意程式碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [BinScope 工具參考](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| 遵守系統重新開機管理員訊息                                       | 當使用者啟動關機時，在大部分的情況下，他們都強烈希望能夠看到關機成功;他們可能會想要離開辦公室並「只想」他們的電腦關閉。 應用程式必須遵守此需求，而不會封鎖關機。 雖然在大部分情況下，關閉可能不會很重要，但應用程式必須針對重大關機的可能性做好準備。                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Windows Vista 中的應用程式關閉變更](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [重新開機管理員開發](/previous-versions/bb756958(v=msdn.10))<br/>                                                                                                                                                                                                                                                                                                                        |
| 乾淨的可還原安裝                                                   | 乾淨、可還原的安裝可讓使用者順利管理 (在其系統上部署和移除) 應用程式。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [如何：使用 ClickOnce 應用程式安裝必要條件](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [64位系統上的應用程式安裝](/windows/desktop/WinProg64/application-installation)<br/>                                                                                                                                                                                                                                                                                          |
| 數位簽署檔案和驅動程式                                                | Authenticode 數位簽章可讓使用者確認軟體是否為正版。 它也可讓您偵測檔案是否已遭篡改，例如，是否已受到病毒感染。 核心模式程式碼簽署強制是一項稱為程式碼完整性 (CI) 的 Windows 功能，可在每次將檔案映射載入記憶體時驗證檔案的完整性，藉此改善作業系統的安全性。 CI 會偵測惡意程式碼是否已修改系統二進位檔案。 當核心模組的簽章無法正確確認時，也會產生診斷和系統審核記錄事件。                                                                                                                                                                            | [Windows 上核心模組的數位簽章](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| 請勿根據作業系統版本檢查封鎖安裝或應用程式啟動 | 當客戶沒有技術限制時，請務必讓客戶無法安裝或執行其應用程式。 一般來說，如果應用程式是針對 Windows Vista 或更新版本所撰寫，則應該沒有理由檢查作業系統版本。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [作業系統版本控制](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 請勿在保管庫模式中載入服務和驅動程式                                   | 保管庫模式可讓使用者診斷 Windows 並進行疑難排解。 除非系統的基本作業需要 (例如，儲存設備磁碟機) 或用於診斷和復原用途 (例如，防毒程式) 、驅動程式和服務不得設定為以安全模式載入。 根據預設，安全模式不會啟動未預先安裝 Windows 的大部分驅動程式和服務。 除非系統需要它們進行基本作業或用於診斷和復原，否則應保持停用。                                                                                                                                                                                                                                                                                         | [判斷作業系統是否正在保管庫模式下執行](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [如何判斷系統是否以設備磁碟機的保管庫模式執行](https://support.microsoft.com/kb/837643)<br/>                                                                                                                                                                                                                                                 |
| 遵循使用者帳戶控制 (UAC) 指導方針                                    | 某些 Windows 應用程式會在系統管理員帳戶的安全性內容中執行，而許多應用程式需要過多的使用者權限和 Windows 許可權。 控制資源的存取權，可讓使用者控制其系統免于不必要的變更 (不必要的變更可能是惡意的，例如接管電腦的 rootkit 暗中;，或是具有有限許可權之人員的動作，例如，將禁止的軟體安裝在工作電腦上的員工) 。 控制資源存取最重要的規則就是提供使用者執行其必要工作所需的最少量存取標準使用者內容。 遵循 UAC 指導方針可在需要時提供應用程式必要的許可權，而不會讓系統持續暴露于安全性風險。 | [使用者帳戶控制](/windows/desktop/uxguide/winenv-uac)<br/> [UAC：應用程式更新指導方針](/previous-versions/aa480152(v=msdn.10))<br/>                                                                                                                                                                                                                                                                                                                 |
| 依預設安裝到正確的資料夾                                       | 使用者的預設安裝位置應該具有一致且安全的體驗，同時保有將應用程式安裝至所選位置的選項。 此外，您也必須將應用程式資料儲存在正確的位置，以允許多人使用同一部電腦，而不會損毀或覆寫彼此的資料和設定。                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [安裝/卸載需求摘要](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 支援多使用者會話                                                     | Windows 的使用者應該能夠在不發生衝突或中斷的情況下執行並行會話。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [遠端桌面服務程式設計指導方針](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| 支援 Windows 的 x64 版本                                                 | 隨著64位硬體越來越普及，使用者期望應用程式開發人員將其應用程式遷移至64位，或應用程式的32位版本在 Windows 的64位版本下執行，以利用64位架構的優點。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [應用程式相容性： Windows Vista 64 位](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |





## <a name="see-also"></a>另請參閱

-   [Windows硬體認證計畫](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))
-   [WindowsStore Apps 認證需求](/legal/windows/agreements/store-policies)
-   [Windows 7 軟體標誌計畫](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)
-   [如何使用 Windows 應用程式認證套件](./using-the-windows-app-certification-kit.md)
