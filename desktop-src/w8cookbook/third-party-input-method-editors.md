---
title: 協力廠商輸入法編輯器
description: 協力廠商輸入法編輯器
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca9768de96b9dcdeac7f4b0da210f7aa788801b
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104562795"
---
# <a name="third-party-input-method-editors"></a>協力廠商輸入法編輯器

## <a name="platforms"></a>平台

**客戶** 端-Windows 8  
**伺服器** -Windows Server 2012  


## <a name="description"></a>Description

輸入法編輯器 (Ime) 是軟體元件，可讓使用者輸入比在鍵盤上可以表示更多字元的語言文字。  (這種情況很常見，但不限於東亞語言。 ) ，而不是每個出現在單一按鍵上的單一字元，使用者可以輸入輸入法所轉譯的按鍵組合。 IME 會產生符合一組按鍵筆劃的字元，有時會向使用者呈現可從中挑選的可能字元清單，然後將該字元插入使用者應用程式的 [編輯] 控制項視窗中。

在過去，Windows 已允許協力廠商的 Ime 在 Windows 系統中執行，而這項功能會繼續進行 Windows 8。 使用者可以安裝協力廠商的輸入法，並加以使用。 此外，我們也強化了系統和程式，以防止惡意的 Ime、提升安全性，以及強化使用者體驗。

在 Windows 8 中，您將會發現：

-   硬體鍵盤和觸控鍵盤的協力廠商 IME 支援
-   協力廠商 IME 廠商必須遵循 Microsoft 指導方針來開發其 Ime 以進行 Windows 8
-   協力廠商 Ime 必須經過數位簽署
-   協力廠商 Ime 必須是文字服務架構 (TSF) 感知，而且必須將適當的 IME 旗標設定為在 Windows 8 中正確執行。
-   舊版的協力廠商 Ime 將能夠在桌面應用程式中執行，但在 Windows Store 應用程式中會遭到封鎖
-   協力廠商 Ime 可以使用 Windows 所提供的觸控鍵盤配置來連結其 IME，讓使用者可以使用其 IME 搭配觸控鍵盤。 不過，協力廠商 Ime 將無法使用適用于觸控鍵盤的內建 Ime 功能
-   Windows Defender 會從 Windows 系統移除惡意的 Ime

## <a name="manifestation"></a>表現

**輸入語言和輸入方法切換變更**

並不會顯示所有 IME 模式圖示，以及輸入法商標圖示，只會顯示一個 IME 模式圖示以及輸入法商標圖示。 下列兩個圖形顯示 Windows 8 輸入飛出視窗和輸入法飛出視窗，以日文 IME 作為目前的輸入方法。 如果您按一下 [IME 商標] 圖示，就可以切換輸入方法。

![切換輸入方法](images/inputindicator2.png)

如果您按一下輸入法模式圖示，就可以切換到不同的 IME 模式。

![切換輸入法模式](images/inputindicator1.png)

如果 IME 依賴語言列在 Windows 7 中顯示其模式圖示，則必須變更 IME，才能在 Windows 8 的輸入指標中顯示其商標圖示和模式圖示。

> [!Note]  
> 注意：在桌面工作列上的工作列中，IME 如何顯示商標圖示和模式圖示的詳細資料，將會以 Windows 8 IME 指導方針的方式記載並公佈。

 

**新的 Windows 環境**

Windows 8 中的環境會變更 Ime 的橫向。 Windows 7 不提供 Windows Store 應用程式的概念、本機內容應用程式容器，以及對 Ime 的 API 限制。 某些現有的 Windows 7 Ime 在 Windows Store 應用程式內執行時停止回應，因此不允許在 Windows Store 應用程式內執行舊版 Ime。 此外，請確定已驗證新版本的 Ime，以確保它們在 Windows Store 應用程式內執行之前，都能與新的 UI 環境相容。

## <a name="mitigation"></a>降低

您可以在系統上使用桌面相容的 IME。 如果您主要是使用桌面應用程式，而您想要繼續使用慣用的舊版 IME 進行輸入，這可能是您的最佳選擇。 建議您使用 Windows 8 IME，並停止使用舊版/非認證的 Ime。 通知是由語言 CPL 和輸入參數提供，以警告您使用桌面相容 IME 的效果。

如果電腦相容的 IME 無法在您的系統上運作，您將會看到下列其中一種行為：

-   語言 CPL UI 會將桌面相容的 Ime 標記為標籤，並顯示一則訊息，指出不相容的 Ime 只能在桌面應用程式中運作。
-   當使用者在 Windows Store 應用程式中時，輸入飛出視窗會 greys 桌面相容的 Ime。 這表示輸入法無法在此應用程式中運作。 桌上型電腦相容的 Ime 在桌面上 (不會呈現灰色) 。 如果您使用不相容的輸入法切換至 Windows Store 應用程式，併發現輸入法是 off，請使用輸入指標來變更為與 Windows Store 應用程式相容的 IME。

舊版或桌面相容的 Ime 僅限於下列條件：

-   從 Windows 7 升級至 Windows 8，並在系統上使用協力廠商的 Ime
-   廠商尚未發行與 Windows 8 相容的版本，使用者同時嘗試使用現有的 Windows 7 版本

## <a name="solution"></a>解決方法

**一般**

使用現有的文字服務架構 (TSF) 基礎結構，為您的 Ui 執行您的 IME 邏輯和 Windows Store 應用程式通用控制項。 建立擁有的 windows 來裝載您的 UI。

新增搜尋 Api 是為了改善搜尋預測，並在 UI 中提供簡潔的搜尋體驗。

此外，也會新增 Api，以在叫用觸控鍵盤時通知協力廠商 Ime，以防止觸摸鍵盤涵蓋 UI。 協力廠商 Ime 會自動載入預設的傳統觸控鍵盤配置。 不需要額外的工作就能與此傳統觸控鍵盤配置整合。 但是，協力廠商的 Ime 將能夠要求替代的觸控版面配置。

熟悉 Windows 8 IME 指導方針，讓您可以在您的 IME 中升級重要的 Windows Store 應用程式使用者經驗準則。 遵循指導方針的 Ime 必須設定旗標，以指出 IME 與 Microsoft 設計相容。 Windows 8 封鎖所有與桌面相容的 Ime 在 Windows Store 應用程式中執行。

數位簽章除了 Windows Defender 撤銷之外，還能防止將惡意的 Ime 安裝到 Windows 8 系統上。 身分識別驗證之後，會以數位方式簽署協力廠商輸入的 .dll。 只有具有這個數位簽章的 Ime 可以安裝到系統上，而不會對使用者顯示重大警告訊息。 使用者可以報告惡意的 Ime。 當 IME 判斷為惡意之後，Windows Defender 會將它從 Windows 系統中移除。

**Text Services Framework (TSF)**

IME 必須是 TSF 感知，才能在 Windows 8 中執行。 Windows 8 封鎖在 Windows Store 應用程式中執行的非 TSF 感知 Ime。 當應用程式啟動時，TSF 會針對使用者已選取到應用程式進程中的 IME 載入輸入輸入。

> [!Note]  
> 為了在 Windows Store 應用程式與桌面應用程式之間提供個別的功能或 Ui，TSF 所載入的 .dll 可以檢查載入的應用程式類型。 IME 會呼叫 [ITfThreadMgrEx：： GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) 方法，並檢查 TF \_ TMF \_ IMMERSIVEMODE 旗標，並根據結果觸發不同的應用程式邏輯。

 

當 IME 載入至 Windows Store 應用程式時，它會受限於與應用程式本身相同的應用程式容器限制。 這種行為可確保 Ime 無法違反 Windows Store 應用程式安全性合約，儘管可以存取桌面 SDK (，因為它們不是由 Windows Store) 發佈或認證。 某些 Ime 目前執行的函式會在應用程式容器內受到影響。 這些函數包括：

-   字典檔
-   網際網路更新
-   即時學習
-   在進程之間共用資訊

如需詳細資訊，請參閱 Windows 8 IME 指導方針。

舊版 Ime 無法在 Windows Store 應用程式中運作，以避免可能發生不正確的使用者體驗，包括系統阻礙。 與 Windows Store 應用程式相容的 Ime 必須透過設定指出此相容性的旗標來自我宣告。 此旗標是由 TF INPUTPROCESSORPROFILE 結構中的 TSF 所提供 \_ 。 有關如何使用此旗標將協力廠商 IME 宣告為 Windows Store 應用程式相容的詳細資料，將會記載並公佈在 Windows 8 IME 指導方針中。

您可以在桌面應用程式或 Windows Store 應用程式中，執行與 Windows Store 應用程式相容的 Ime。 不相容的 Ime 只能在桌面進程中執行。

**User Interface** (使用者介面)

雖然協力廠商 Ime 可以存取桌面視窗化 Api，但它們必須遵循與執行應用程式相同的 windows API 限制。 例如，在傳統型應用程式中使用中時，IME 無法在 Windows Store 應用程式上繪製。 API 限制的目標是要避免這些情況：

-   從 Windows Store 應用程式取得焦點的桌面應用程式
-   Windows Store 應用程式中的桌面應用程式繪圖
-   桌面應用程式干擾 Windows Store 應用程式

**觸控鍵盤支援**

雖然觸控鍵盤 (TKB) 支援仍然可供協力廠商的 IME 廠商使用，但 Windows 8 中不提供可完全自訂和整合的觸控鍵盤體驗。 但是，協力廠商 Ime 可以對應其 Ime 與針對觸控優化的鍵盤配置。 Windows 軟輸入面板 (SIP) 預設會提供協力廠商 Ime 的傳統鍵盤配置。 由於傳統鍵盤產生的按鍵事件與硬體鍵盤的運作方式類似，因此協力廠商的 Ime 目前沒有特殊的執行需求可使用觸控鍵盤。 硬體金鑰事件的輸入處理也會處理來自傳統觸控配置的重要事件。

> [!Note]  
> 注意：如果 TKB 支援已擴充為包含優化的鍵盤配置，則 Ime 可能需要開始處理 Unicode 輸入事件。

 

協力廠商 IME 可以選擇針對其 IME 使用優化的鍵盤配置。 如需詳細資訊，請參閱協力廠商輸入法指導方針。

確定您的候選窗格的 UI (和其他 UI 元素) 不會繪製在觸摸鍵盤之下。 在大部分情況下，應用程式應調整其視窗的大小，以考慮觸控鍵盤。 但是，如果應用程式沒有這麼做，Ime 仍可以使用 InputPaneFramework API 來瞭解觸控鍵盤的位置。 協力廠商 Ime 可以使用此 API 來取得觸控鍵盤在繪製候選 (或其他) Ui 之前所耗用的螢幕空間，以及重新排列其 UI，以避免在觸摸鍵盤下進行繪製。

**搜索**

在 Windows 8 中，Windows Store 應用程式可以藉由執行 [搜尋合約](/previous-versions/windows/apps/hh464906(v=win.10)) 並與 [搜尋] 窗格整合，輕鬆地為使用者提供搜尋功能。 [搜尋] 窗格是讓使用者在所有應用程式中執行搜尋的中心位置。 Windows 可協助使用 [搜尋] 窗格的應用程式，讓他們的使用者盡可能快速地前往。 尤其是針對 IME 使用者，它提供了獨特的搜尋體驗，可讓相容的 Ime 與 Windows 8 整合，以提高效率和可用性。

如果 IME 符合下列準則，則 IME 與整合式搜尋體驗相容：

-   與 Windows Store 應用程式環境相容
-   實行 TFS UILess 模式 Api
-   實行 TFS 搜尋整合 Api：
-   -   ItfSearchCandidateProvider
    -   ItfSearchHardwareKeyboardBehaviors

在 [搜尋] 窗格中啟用時，相容的 IME 會置於 UILess 模式，而且無法顯示其 UI。 相反地，它會將轉換候選項目傳送給 Windows，然後將其顯示在內嵌候選清單控制項中。

IME 也會傳送應該用來執行目前搜尋的 Windows 候選項目，這些候選項目可以與轉換候選項目相同，或可針對搜尋量身打造。 良好的搜尋候選人符合下列準則：

-   沒有前置詞重迭
-   沒有僅限完成的預測候選 () 

不符合準則且與搜尋不相容的 Ime 會以與其他 Windows Store 應用程式控制的相同方式顯示，而且無法利用 UI 整合和搜尋候選項目。  (的應用程式只會在使用者撰寫完成之後才接收查詢。 ) 

當支援搜尋合約的應用程式收到查詢時，查詢事件將會包含 "queryTextAlternatives" 陣列，其中包含所有已知的替代方案，並根據最相關的 (可能) 最相關的 (不太可能) 。 每當提供替代專案時，應用程式應該將每個替代方案視為查詢，並傳回符合任何替代專案的所有結果 (如同使用者已同時發出多個查詢) ，基本上是對提供結果的服務發出「或」查詢。 為了增強效能，應用程式通常會限制比對10個最相關的替代方案。

**IME 數位簽章**

所有協力廠商的 Ime 都必須經過數位簽署，才能安裝到 Windows 8 系統作為 IME。 使用 SmartScreen 時，使用者可以在從 web 下載未簽署的 IME 時看到警告訊息。 取得憑證並簽署檔案：

-   **使用 Authenticode 簽章以數位方式簽署程式**
    -   從 Windows 支援的許多憑證授權單位單位之一取得有效的 Authenticode 程式碼簽署憑證
    -   使用開發工具 (例如 [signtool.exe](../seccrypto/signtool.md)) 來簽署應用程式，再進行散發
    -   如需程式碼簽署程式的詳細資訊和逐步說明，請參閱 [Authenticode 程式碼簽署](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing) blog 專案的須知事項
-   **確定未偵測到下載為惡意程式碼**
    -   偵測到並確認為惡意程式碼的下載程式，會影響下載的信譽以及用來簽署該檔案的數位憑證信譽
-   **適用于 Windows 認證**
    -   造訪 MSDN 上的 Windows 應用程式認證頁面

如需詳細資訊，請參閱下列有關數位簽章和程式碼簽署的文章：

-   [Authenticode 總覽](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [確保完整性和真實性](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [什麼是數位憑證？](/previous-versions/office/developer/office2000/aa190113(v=office.10))

如果 **未** 簽署 ime，當使用者嘗試下載 ime 時，會收到這個警告訊息：

![輸入法未簽署警告訊息](images/downloadwarning02-fhu-ivu.png)

如果 IME 經過簽署，使用者會看到下列訊息：

![ime 是已簽署的訊息](images/downloadwarning01-fhu-vcu.png)

根據這些通知，使用者可以選擇是否要刪除檔案，或忽略警告並執行下載的程式。

**IME 撤銷**

您可以使用 Windows Defender，從系統中移除惡意或未遵循 Windows 8 IME 指導方針的 Ime。 如需有關惡意 Ime 的詳細資訊，請參閱 [Windows 8 中的協力廠商 ime](/previous-versions/windows/apps/hh967426(v=win.10))的相關文章。

## <a name="resources"></a>資源

-   [ITfThreadMgrEx：： Get Active Flags 方法](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Authenticode 程式碼簽署的所有須知](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Windows 應用程式合約和延伸模組](/previous-versions/windows/apps/hh464906(v=win.10))
-   [Windows 8 桌面應用程式的認證需求](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Windows 應用程式的認證需求](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [使用 Windows 應用程式認證套件](../win_cert/using-the-windows-app-certification-kit.md)
-   [Authenticode 總覽](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [確保完整性和真實性](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [什麼是數位憑證？](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 