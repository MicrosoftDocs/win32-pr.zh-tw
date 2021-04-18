---
title: Windows 應用程式認證套件測試
description: 以下是認證 dekstop apps 的測試詳細資料。
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a353eef0cd73fecac275b750345b3dd97d05dc87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965249"
---
# <a name="windows-app-certification-kit-tests"></a>Windows 應用程式認證套件測試

以下是認證 dekstop apps 的測試詳細資料。 如需詳細資訊，請參閱 [使用 Windows 應用程式認證套件](using-the-windows-app-certification-kit.md)。

-   [清除可還原的安裝](#clean-reversible-install)
-   [安裝到正確的資料夾測試](#install-to-the-correct-folders-test)
-   [經過數位簽署的檔案測試](#digitally-signed-file-test)
-   [支援 x64 Windows 測試](#support-x64-windows-test)
-   [作業系統版本檢查測試](#os-version-checking-test)
-   [ (UAC) 測試的使用者帳戶控制](#user-account-control-uac-test)
-   [遵守系統重新開機管理員訊息](#adhere-to-system-restart-manager-messages)
-   [安全模式測試](#safe-mode-test)
-   [多使用者會話測試](#multiuser-session-test)
-   [當機和停止回應測試](#crashes-and-hangs-test)
-   [相容性與復原能力測試](#compatibility-and-resiliency-test)
-   [Windows 安全性最佳作法測試](#windows-security-best-practices-test)
-   [Windows 安全性功能測試](#windows-security-features-test)
-   [高 DPI 測試](#high-dpi-test)

## <a name="clean-reversible-install"></a>清除可還原的安裝

安裝和卸載應用程式，並檢查剩餘的檔案和登錄專案。

-   背景
    -   乾淨且可還原的安裝可讓使用者部署和移除應用程式。 若要通過此測試，應用程式必須執行下列動作：
        -   安裝或卸載應用程式之後，應用程式不會強制系統立即重新開機。 *應用程式的安裝或卸載程式在完成後，應該永遠不需要重新開機系統。如果需要重新開機系統，使用者應該能夠在方便的情況下重新開機系統。*
        -   應用程式不會相依于 8.3 (SFN) 的簡短檔案名。 *應用程式的安裝和卸載程式必須能夠使用長檔名和資料夾路徑。*
        -   應用程式不會封鎖無訊息安裝/卸載
        -   應用程式會在系統登錄中建立必要的專案。 *Windows 清查工具和遙測工具需要已安裝應用程式的完整資訊。應用程式安裝程式必須建立正確的登錄專案，以允許偵測和卸載成功。*
    -   如果您使用以 MSI 為基礎的安裝程式，MSI 會自動建立下面的登錄專案。 如果您不是使用 MSI 安裝程式，則安裝模組必須在安裝期間建立下列登錄專案：
        -   DisplayName
        -   InstallLocation
        -   Publisher
        -   UninstallString
        -   VersionMajor 或 MajorVersion
        -   VersionMinor 或 MinorVersion
    -   應用程式必須移除其在 [新增/移除程式] 中的所有專案。
-   測試詳細資料
    -   此測試會檢查應用程式的安裝和卸載程式，以取得所需的行為。
-   更正動作
    -   根據上述需求來檢查應用程式的設計和行為。

## <a name="install-to-the-correct-folders-test"></a>安裝到正確的資料夾測試

確認應用程式將其程式和資料檔案寫入正確的資料夾。

-   背景
    -   應用程式必須正確地使用使用者系統和每個使用者資料夾，讓它可以存取所需的資料和設定，同時保護使用者的資料和設定，防止未經授權的存取。
-   Program Files 資料夾
    -   根據預設，應用程式必須安裝在 Program Files 資料夾中， ( 原生32位和64位應用程式的% ProgramFiles%，以及在 x64) 上執行32位應用程式的% ProgramFiles (x86) %。
    -   **注意：** 應用程式不能將使用者資料或應用程式資料儲存在 Program Files 資料夾中，因為已為此資料夾設定安全性許可權。
    -   Windows 系統資料夾上的 Acl 只允許系統管理員帳戶讀取和寫入它們。 因此，標準使用者帳戶將無法存取這些資料夾。 不過，檔案虛擬化可讓應用程式將檔案（例如設定檔）儲存在通常只能由系統管理員進行寫入的系統位置中。 在這種情況下，以標準使用者的形式執行程式可能會在無法存取必要的檔案時導致失敗。
    -   應用程式應該使用 [已知的資料夾](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) ，以確保它們可以存取其資料。
    -   **注意：** Windows 提供檔案虛擬化來改善應用程式相容性，並消除當應用程式在 Windows 上以標準使用者的形式執行時的問題。 您的應用程式不應該依賴虛擬化存在未來的 Windows 版本。
-   使用者特定的應用程式資料檔案夾
    -   在「個別電腦」安裝中，應用程式不能在安裝期間寫入使用者專屬的資料。 只有在使用者第一次啟動應用程式時，才應寫入使用者特定安裝資料。 這是因為沒有正確的使用者位置可在安裝時儲存資料。 在安裝之後，應用程式嘗試修改電腦層級的預設關聯線為將會失敗。 相反地，預設值必須在每個使用者層級宣告，如此可防止多個使用者覆寫彼此的預設值。
    -   特定使用者專屬的所有應用程式資料，而不是與電腦的其他使用者共用，則必須儲存在使用者 \\ <username> \\ AppData 中。
    -   必須在電腦上的使用者之間共用的所有應用程式資料都應儲存在 ProgramData 中。
-   其他系統資料夾和登錄機碼
    -   應用程式永遠不應該直接寫入 Windows 目錄和或子目錄。 使用正確的方法，將檔案（例如字型或驅動程式）安裝至這些目錄。
    -   應用程式不應該在啟動時自動啟動，例如將專案新增至下列其中一個或多個位置：
        -   登錄執行金鑰 HKLM、或軟體 \\ Microsoft \\ Windows \\ CURRENTVERSION 下的 HKCU
        -   登錄執行金鑰 HKLM 和或 HKCU 下的 Software \\ Wow6432Node \\ Microsoft \\ windows \\ CurrentVersion
        -   開始功能表 AllPrograms > 啟動
-   測試詳細資料
    -   這項測試會驗證應用程式是否使用 Windows 提供的檔案系統中的特定位置，來儲存程式和軟體元件、共用應用程式資料，以及使用者特定的應用程式資料。
-   修正動作
    -   請參閱應用程式如何使用系統的資料夾，並確定它使用的是正確的。
-   例外狀況和豁免
    -   寫入全域組件快取 (GAC 的桌面應用程式必須要有棄權)  ( .NET 應用程式應該將元件相依性保留為私用，並將其儲存在應用程式的目錄中，除非) 中明確需要共用元件。
    -   只有在 SW 基礎類別下，才需要安裝 [program Files] 資料夾，才能達成 SW 標誌。

## <a name="digitally-signed-file-test"></a>經過數位簽署的檔案測試

測試可執行檔和設備磁碟機，以確認它們具有有效的數位簽章。

-   背景
    -   數位簽署的檔案可讓您確認檔案是否為正版，以及偵測檔案是否已遭修改。
    -   核心模式程式碼簽署強制是一項 Windows 功能，也稱為程式碼完整性 (CI) 。 CI 會在每次將檔案載入記憶體時驗證其完整性，藉以改善 Windows 的安全性。 CI 會偵測是否有惡意程式碼修改系統二進位檔案，並在核心模組的簽章無法正確確認時，產生診斷和系統審核記錄事件。
    -   如果應用程式需要較高的許可權，提高許可權提示會顯示要求提升存取權之可執行檔的相關內容資訊。 視應用程式是否經過 Authenticode 簽署而定，使用者可能會看到同意提示或認證提示。
    -   強式名稱可防止協力廠商詐騙您的程式碼，只要您將私密金鑰保持安全。 .NET Framework 會在載入元件時驗證數位簽章，或將它安裝在 GAC 中。 如果沒有私密金鑰的存取權，惡意使用者就無法修改您的程式碼並重新簽署。
-   測試詳細資料
    -   所有可執行檔（例如副檔名為 .exe、.dll、.ocx、sys、winspool.drv 和 .scr 的檔案）都必須使用 Authenticode 憑證進行簽署。
    -   應用程式安裝的所有核心模式驅動程式都必須具備透過 WHQL 或 DRS 程式取得的 Microsoft 簽章。 所有檔案系統篩選器驅動程式都必須經過 WHQL 簽署。
-   更正動作
    -   簽署應用程式的可執行檔。
    -   使用 makecert.exe 來產生憑證，或從) 的其中一個商業憑證發行 (機構單位（例如 VeriSign、Thawte 或 Microsoft CA）取得程式碼簽署金鑰。
-   例外狀況和豁免
    -   只有未簽署的協力廠商可轉散發套件才會考慮豁免。 若要授與此棄權的要求，必須對要求籤署版本的可轉散發套件 () s 進行通訊證明。
    -   裝置值新增的軟體套件豁免于核心模式驅動程式憑證，因為驅動程式必須由 Windows 硬體認證認證。

## <a name="support-x64-windows-test"></a>支援 x64 Windows 測試

測試應用程式，以確定 .exe 是針對將安裝的平臺架構所建立。

-   背景
    -   可執行檔必須針對安裝它的處理器架構建立。 某些可執行檔可能會在不同的處理器架構上執行，但是這並不可靠。
    -   架構相容性很重要，因為32位進程無法載入64位 Dll，而64位進程無法載入32位 Dll。 同樣地，64位版本的 Windows 不支援執行以16位 Windows 為基礎的應用程式，因為控制碼在64位 Windows 上具有32個有效位，因此無法將它們傳遞給16位應用程式。 因此，嘗試啟動16位應用程式將會在64位版本的 Windows 上失敗。
    -   32位設備磁碟機無法在64位版本的 Windows 上執行，因此必須將它們移植到64位架構。
    -   在使用者模式應用程式中，64位 Windows 包含 WOW64，可讓32位 Windows 應用程式在執行64位 Windows 的系統上執行，儘管效能會降低。 設備磁碟機沒有對等的轉譯層存在。
    -   為了維持與64位版本 Windows 的相容性，應用程式必須以原生方式支援64位，或者，至少32位的 Windows 應用程式必須在64位系統上順暢地執行：
        -   應用程式及其安裝程式不得包含任何16位程式碼，或依賴任何16位元件。
        -   應用程式安裝程式必須在64位版本的 Windows 上偵測並安裝適當的驅動程式和元件。
        -   任何 shell 外掛程式都必須在64位版本的 Windows 上執行。
        -   在 WoW64 模擬器下執行的應用程式不應該嘗試略過 Wow64 虛擬化機制。 如果有應用程式需要偵測到在 WoW64 模擬器中執行的特定案例，則應該呼叫 [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)來執行此動作。
-   測試詳細資料
    -   應用程式不應該安裝任何16位二進位檔。 如果應用程式應該在64位電腦上執行，則應用程式不應安裝32位核心模式驅動程式。
-   更正措施
    -   針對您要安裝的處理器架構，建立可執行檔和驅動程式。

## <a name="os-version-checking-test"></a>作業系統版本檢查測試

測試應用程式如何檢查正在執行的 Windows 版本。

-   背景
    -   應用程式會藉由測試大於或等於所需版本的版本來檢查作業系統版本，以確保與未來版本的 Windows 相容。
-   測試詳細資料
    -   模擬在不同版本的 Windows 上執行應用程式，以查看其回應方式。
-   修正動作
    -   測試目前版本是否大於或等於您的應用程式、服務或驅動程式所需的版本，以測試正確的 Windows 版本。
    -   驅動程式安裝程式和卸載模組絕不能檢查作業系統版本。
-   例外狀況和豁免
    -   將會針對符合下列準則的應用程式考慮豁免： *(僅適用于桌面應用程式認證)*
        -   在 Windows XP、Windows Vista 和 Windows 7 上以一個套件的形式傳遞的應用程式，而且需要檢查作業系統版本，以判斷要在指定的作業系統上安裝哪些元件。
        -   只有在安裝期間只會檢查作業系統的最小版本 (的應用程式，而不是在執行時間) 只使用核准的 API 呼叫，並在應用程式資訊清單中列出必要的最低版本需求。
        -   安全性應用程式，例如防毒軟體和防火牆應用程式、系統公用程式（例如重組公用程式和備份應用程式），以及只使用核准的 API 呼叫來檢查作業系統版本的診斷工具。

## <a name="user-account-control-uac-test"></a> (UAC) 測試的使用者帳戶控制

測試應用程式，以確認它不需要更高的許可權來執行。

-   背景
    -   只有當使用者為系統管理員時，才會操作或安裝的應用程式會強制使用者以不必要的提高許可權來執行應用程式，這可讓惡意程式碼進入使用者的電腦。
    -   當使用者一律強制執行具有更高存取權杖的應用程式時，應用程式可以做為詐騙或惡意程式碼的進入點。 這種惡意程式碼可輕鬆地修改作業系統（或更糟的）來影響其他使用者。 您幾乎無法控制具有完整系統管理員存取權的使用者，因為系統管理員可以安裝應用程式，並在電腦上執行任何應用程式或腳本。 IT 管理員一直都在尋求在使用者以標準使用者身份登入的情況下，建立「標準桌面」的方法。 標準桌面可大幅降低技術支援中心的成本，並降低 IT 額外負荷。
    -   大部分的應用程式在執行時間並不需要系統管理員許可權。 標準使用者帳戶應該能夠執行這些工作。 Windows 應用程式必須有 (embedded 或 external) 的資訊清單，才能定義其執行層級，以告訴 OS 執行應用程式所需的許可權。 應用程式資訊清單只適用于 .exe 檔案，而不是 .dll 檔案。 使用者帳戶控制 (UAC) 不會在進程建立期間檢查 Dll。 UAC 規則不適用於 Microsoft 服務。 應用程式資訊清單可以是內嵌或外部。
    -   若要建立資訊清單，請建立名為 <應用程式 \_ 名稱 # C1.exe 的檔案，並將它儲存在與 EXE 相同的目錄中。 請注意，如果應用程式具有內部資訊清單，則會忽略任何外部資訊清單。
        -   例如，<並無 requestedexecutionlevel level = "" asInvoker \| highestAvailable \| requireAdministrator "" uiAccess = "" true \| false ""/>
        -   應用程式的主要處理常式必須以標準使用者的形式執行 (**asInvoker**) 。 任何系統管理功能都必須移至以系統管理許可權執行的個別進程。
        -   需要較高許可權的使用者面向應用程式必須經過 Authenticode 簽署。
-   測試詳細資料
    -   所有面向使用者的 exe 都應該以 asInvoker 屬性標記。 如果它們被標示為 highestAvailable 或 requireAdministrator，則應該正確地簽署 authenticode。 任何應用程式 exe 都不應將 uiAccess 屬性設定為 true。 以服務方式執行的任何 exe 都會從此特定檢查中排除。
-   修正動作
    -   請檢查應用程式的資訊清單檔，以取得正確的專案和許可權等級。
-   例外狀況和豁免
    -   以更高的許可權執行其主要進程的應用程式需要棄權 (**requireAdministrator** 或 **highestAvailable**) 。 主要進程是提供使用者進入應用程式進入點的程式。
    -   在下列案例中，將會考慮棄權：
        -   執行層級設為 **highestAvailable**、 **requireAdministrator** 或兩者的系統管理或系統工具。
        -   只有協助工具或 UI 自動化架構應用程式會將 uiAccess 旗標設為 TRUE，以略過使用者介面許可權隔離 (UIPI) 。 若要適當地開始使用應用程式，此旗標必須經過 Authenticode 簽署，而且必須位於檔案系統中受保護的位置，例如 Program Files。

## <a name="adhere-to-system-restart-manager-messages"></a>遵守系統重新開機管理員訊息

測試應用程式如何回應系統關機和重新開機訊息。

-   背景
    -   應用程式必須在系統正在關機時儘快結束，以提供回應式關機或使用者的電源關閉體驗。
    -   在重大關機中，傳回 FALSE 到 [**wm \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) 的應用程式將會傳送至 wm **\_ ENDSESSION** 且已關閉，而這些應用程式會 \_ 被強制終止。
-   測試詳細資料
    -   檢查應用程式如何回應關機和結束訊息。
-   修正動作
    -   如果您的應用程式未通過此測試，請參閱其處理這些 Windows 訊息的方式：
        -   [**WM \_QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) with *LPARAM*  =  **ENDSESSION \_ CLOSEAPP** (0x1) ：桌面應用程式必須在準備重新開機時立即回應 (TRUE) 。 主控台應用程式可以呼叫 [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) 來接收關機通知。 服務可以呼叫 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) ，以接收處理常式常式中的關機通知。
        -   [**WM \_ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) with *LPARAM*  =  **ENDSESSION \_ CLOSEAPP** (0x1) ：應用程式必須在30秒內傳回0值，並將其關閉。 應用程式至少應該藉由儲存任何使用者資料，並在重新開機之後指出所需的資訊，來做好準備。
    -   接收 **CTRL + \_ \_ 事件** 通知的主控台應用程式應該立即關閉。 驅動程式不得拒絕系統關機事件。
    -   **注意：** 因為無法中斷的作業而必須封鎖關機的應用程式應該使用 [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) 來註冊說明使用者原因的字串。 當作業完成時，應用程式應該呼叫 [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) 來指示系統可以關機。

## <a name="safe-mode-test"></a>安全模式測試

測試驅動程式或服務是否已設定為以安全模式啟動。

-   背景
    -   安全模式可讓使用者診斷和疑難排解 Windows 的問題。 只有作業系統基本操作或提供診斷和復原服務所需的驅動程式和服務，才能以安全模式載入。 在安全模式中載入其他檔案，可讓您更難排解作業系統的問題。
    -   依預設，只有隨 Windows 預先安裝的驅動程式和服務會以安全模式啟動。 除非系統需要這些驅動程式與服務進行基本作業或用於診斷和復原，否則應停用所有其他驅動程式和服務。
-   測試詳細資料
    -   應用程式所安裝的驅動程式不應標示為以安全模式載入。
-   修正動作
    -   如果驅動程式或服務不應該以安全模式啟動，請從登錄機碼中移除應用程式的專案。
-   例外狀況和豁免
    -   必須以安全模式啟動的驅動程式和服務需要獲得棄權認證。 棄權要求必須包含每個要新增至安全開機登錄機碼的驅動程式和服務，並描述驅動程式或服務必須在安全模式中執行的技術原因。 應用程式安裝程式必須在這些登錄機碼中註冊所有這類驅動程式和服務：
        -   HKLM/System/CurrentControlSet/Control/安全開機/基本
        -   HKLM/System/CurrentControlSet/Control/安全開機/Network
-   **注意：** 您必須測試要在安全模式中啟動的驅動程式和服務，以確保它們在安全模式下運作，而不會發生任何錯誤。

## <a name="multiuser-session-test"></a>多使用者會話測試

測試應用程式在多個會話中執行時的行為。

-   背景
    -   Windows 使用者必須能夠執行並行會話。 應用程式必須確保在本機或遠端執行多個會話時，應用程式的一般功能不會受到負面影響。 應用程式設定和資料檔案必須是使用者專屬的，而且使用者的隱私權和喜好設定必須限制在使用者的會話中。
-   測試詳細資料
    -   執行應用程式的多個並行實例來測試下列各項：
        -   同時執行之應用程式的多個實例會彼此隔離。
    -   這表示另一個實例看不到來自某個實例的使用者資料。 非作用中使用者會話中的音效不應該在使用中的使用者會話中聽到。 在多個應用程式實例使用共用資源的情況下，應用程式必須確保不會發生衝突。
        -   如果已為多個使用者安裝應用程式，則會將資料儲存在正確的資料夾 (s) 和登錄位置。
        -   應用程式可以在多個使用者會話中執行， (快速使用者切換) 用於本機和遠端存取。
    -   若要確保這種情況，應用程式必須檢查應用程式現有實例的其他終端機服務 (TS) 會話。 如果應用程式不支援多個使用者會話或遠端存取，則當使用者從這類會話啟動時，必須明確地將此內容告訴使用者。
-   更正措施
    -   請確定應用程式不會在使用者專屬的資料存放區中儲存整個系統的資料檔案或設定，例如使用者設定檔或 HKCU。 如果有的話，其他使用者就無法使用該資訊。
    -   在安裝期間，您的應用程式必須安裝全系統的設定和資料檔案，並且在使用者執行時建立使用者特定的檔案和設定。
    -   請確定應用程式不會在本機或遠端封鎖多個並行會話。 應用程式不得相依于全域 mutex 或其他命名物件，以檢查或封鎖多個並行會話。
    -   如果應用程式不允許每個使用者有多個並行會話，請針對 mutex 和其他命名物件，使用每個使用者或每個會話的命名空間。

## <a name="crashes-and-hangs-test"></a>當機和停止回應測試

在認證測試期間監視 app，記錄該 app 何時發生當機或停滯情形。

-   背景
    -   應用程式失敗（例如當機和停止回應）對使用者來說是一大幹擾，因而造成挫折。 消除這類失敗可改善應用程式的穩定性和可靠性，整體來說，可為使用者提供更好的應用程式體驗。 停止回應或當機的應用程式會導致使用者遺失資料並產生不良的使用經驗。
-   測試詳細資料
    -   我們會透過認證測試來測試 app 的復原能力和穩定性。
    -   Windows 應用程式認證套件會呼叫 [**IApplicationActivationManager：： ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) 來啟動 Windows Store 應用程式。 為了讓 **ActivateApplication** 啟動 app，必須啟用使用者帳戶控制 (UAC)，而且螢幕解析度至少必須為 1024 x 768 或 768 x 1024。 如果任一條件不符合，您的 app 就無法通過這個測試。
-   更正措施
    -   確定測試電腦上的 UAC 已啟用。
    -   確定您在螢幕夠大的電腦上執行測試。
    -   如果您的 app 無法啟動，但測試平台符合 [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) 的先決條件，則您可以檢閱啟用事件記錄檔以疑難排解問題。 在事件記錄檔中找到這些項目：
        1.  開啟 eventvwr.exe，然後流覽至 [ \\ Windows Logs \\ 應用程式] 節點。
        2.  篩選檢視，顯示事件識別碼：5900-6000。
        3.  查閱記錄項目，尋找說明為什麼應用程式無法啟動的資訊。
    -   疑難排解有問題的檔案，並尋找和修正問題。 重新建置並重新測試應用程式。
-   其他資源
    -   [在軟體發展生命週期內使用應用程式驗證器](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [應用程式驗證器]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [使用應用程式驗證器](https://www.microsoft.com/?ref=go)
    -   [AppInit Dll](https://www.microsoft.com/?ref=go)
    -   [將啟動時間縮到最短 (使用 C#/VB/C++ 和 XAML 的 Windows 市集應用程式)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>相容性與復原能力測試

-   背景
    -   這項檢查會驗證應用程式的兩個層面，也就是應用程式主要可執行檔 (s) 例如，使用者面向的應用程式進入點必須針對相容性進行檢查，以及宣告正確的 GUID。 為了支援這種新的測試，報表會在 [相容性 & 復原] 下有子節點。 如果遺失其中一個或兩個條件，應用程式將會失敗。
-   測試詳細資料
    -   **相容性：** 應用程式必須完全正常運作，而不需要使用 Windows 相容性模式、AppHelp 訊息或其他相容性修正程式。 相容性資訊清單可讓 Windows 在不同版本的作業系統下提供應用程式適當的相容行為
    -   **AppInit：** 應用程式不能列出要在 HKEY 本機電腦軟體中載入的 Dll \_ \_ \\ \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit dll 登錄機 \_ 碼。
    -   **Switchback：** 應用程式必須提供 switchback 資訊清單。 如果遺漏資訊清單，Windows 應用程式認證套件會提供警告訊息。 Windows 應用程式認證套件也會確認資訊清單是否包含有效的 OS GUID。
-   修正動作
    -   修正應用程式使用相容性修正程式的元件。
    -   請確定應用程式不會依賴其功能的相容性修正程式。
    -   確定您的應用程式已列入清單，而且相容性區段包含適當的值
-   其他資訊
    -   如需詳細資訊，請參閱 [AppInit dll](/previous-versions/windows/apps/hh994639(v=win.10)) 。

## <a name="windows-security-best-practices-test"></a>Windows 安全性最佳作法測試

-   背景
    -   應用程式不應變更預設的 Windows 安全性設定
-   測試詳細資料
    -   藉由執行受攻擊面分析器來測試應用程式的安全性。 此方法會將每個測試的失敗分類加入。 例如，某些安全性測試的分類可能包括：
        -   初始化失敗
        -   安全性架構失敗
        -   可能的緩衝區溢位失敗
        -   損毀失敗
    -   如需詳細資訊，請參閱 [這裡](/previous-versions/windows/hh920280(v=win.10))。
-   修正動作
    -   針對測試所識別的問題進行疑難排解並加以修正。 重新建置並重新測試應用程式。

## <a name="windows-security-features-test"></a>Windows 安全性功能測試

-   背景
    -   應用程式必須加入 Windows 安全性功能。 變更預設的 Windows 安全性保護會讓客戶面臨較高的風險。
-   測試詳細資料
    -   執行 BinScope 二元分析器以測試 app 的安全性。 如需詳細資訊，請參閱 [這裡](/previous-versions/windows/hh920280(v=win.10))。
-   修正動作
    -   針對測試所識別的問題進行疑難排解並加以修正。 重新建置並重新測試應用程式。

## <a name="high-dpi-test"></a>高 DPI 測試

強烈建議 Win32 應用程式以 DPI 感知。 這是讓應用程式 UI 在各式各樣的高 DPI 顯示器設定中保持一致良好的關鍵。 在高 DPI 顯示器設定上執行的非 DPI 感知應用程式可能會發生問題，例如 UI 元素、裁剪文字和模糊影像的縮放比例不正確。 有兩種方式可宣告應用程式為 DPI 感知。 其中一個是宣告 DPI。

-   背景
    -   這項檢查會驗證應用程式的兩個層面，主要可執行檔 (s) 例如，使用者面向的應用程式進入點必須針對高 DPI 感知，以及呼叫適當的 Api 來支援高 DPI。 如果遺失其中一個或兩個條件，應用程式將會失敗。 這項檢查將會在桌面報表中引進新的區段，請參閱下列範例。
-   測試詳細資料
    -   當偵測到下列任何一項時，測試將會產生警告：
        -   主要 EXE 不會在其資訊清單中宣告 DPI 感知，也不會呼叫 SetProcessDPIAware API。 如果忘記新增 DPI 感知資訊清單) ， (會警告開發人員。
        -   主要 EXE 不會在其資訊清單中宣告 DPI 感知，但會呼叫 SetProcessDPIAware API (警告開發人員應該使用資訊清單來宣告 DPI 感知，而不是呼叫 API) 。
        -   MainEXE 會在其資訊清單中宣告 DPI 感知，但它也會呼叫 SetProcessDPIAware API (警告開發人員) 不需要呼叫該 API。
        -   針對不是主要 Exe 的二進位檔，如果它們呼叫 API，則不建議) 使用 (呼叫 API 的警告。
-   修正動作
    -   不建議使用 SetProcessDPIAware () 函式。 如果 DLL 在初始化期間快取了 DPI 設定，則在應用程式中叫用 SetProcessDPIAware () 可能會產生競爭條件。 在 DLL 中呼叫 SetProcessDPIAware () 函式並不是很好的作法。
-   其他資訊
    -   [撰寫高 DPI 應用程式](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 