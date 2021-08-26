---
description: 使用家長監護設定 api
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: 使用家長監護設定 api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9dd75565559e8fe52413280e35abf076a57ad6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885814"
---
# <a name="using-parental-controls-settings-apis"></a>使用家長監護設定 api

在記錄之前會討論設定，因為記錄是以使用者的設定為條件。

## <a name="wmi-api-settings-writeread"></a>WMI API 設定寫入/讀取

WMI API 提供的非抽象 (原始) 存取由家長監護基礎結構所具現化的所有設定，如 Wpcsprov. mof 架構檔案中所定義。 設定存放區存在於 \\ 根 \\ CIMV2 \\ 應用程式 \\ WindowsParentalControls 命名空間中，並具有定義架構的下列類別定義。 會注明擴充性元素。

每一電腦：

-   WpcSystemSettings (一個實例) 
    -   AddUser () 和 RemoveUser () 方法，分別為指定的 SID 建立和刪除家長監護設定。
    -   系統會強制執行目前遊戲分級系統的屬性，以及與系統管理員檢查記錄相關的追蹤和通知。
    -   擴充性：唯讀和讀取/寫入 HTTP 應用程式的屬性，以及 web 內容篩選的 URL 豁免清單、Web 內容篩選覆寫識別碼和名稱資源 DLL 路徑與識別碼，以及自訂記錄檔事件的欄位和標頭名稱註冊數目。
-   WpcRatingsSystem (每個已安裝分級系統的一個實例) 
    -   WpcRating (每個評等層級) 的一個實例。
    -   WpcRatingDescriptor (每個評等描述項) 的一個實例。
-   擴充性： WpcExtension (每個已新增) 的 [家長監護] 面板擴充性連結來一個實例。
    -   GUID、子系統、識別碼、映射資源路徑、停用狀態影像資源路徑、可執行檔路徑、顯示名稱資源 DLL 路徑和識別碼、子標題資源 DLL 路徑和識別碼的屬性。

每個控制的使用者：

-   WpcUserSettings (每個受控制使用者的一個實例) 
    -   擁有 SID、家長監護 on/off 旗標、登入/關閉旗標、時間限制 on/off 旗標、覆寫啟用旗標、登入時間遮罩，以及一般應用程式限制 on/off 旗標的屬性。
    -   在 Windows 8 現有的屬性工作表示每小時的前半小時。 已加入新的半小時屬性來代表每個小時的後半部。 引進了額外的新屬性來表示每日額度。

        **Windows 7 和 Windows Vista：** 計時器限制支援1小時的資料細微性。

-   WpcWebSettings (每個受控制使用者的一個實例) 
    -   擁有 SID、篩選開啟/關閉旗標、篩選層級、檔案下載封鎖旗標、未分級的網站封鎖旗標的屬性。
-   WpcUrlOverride (在 URL 覆寫清單中明確允許或拒絕每個 URL 的一個實例，以做為 web 內容篩選的允許/封鎖清單) 
    -   擁有 SID、受影響的 URL、允許/封鎖狀態的屬性。
-   WpcAppOverride (一般應用程式限制應用程式覆寫清單中明確允許的每個路徑一個實例) 
    -   擁有 SID 的屬性。 更安全的規則識別碼、應用程式的路徑。
-   WpcGamesSettings (每個受控制使用者的一個實例) 
    -   擁有 SID 的屬性、允許的遊戲旗標、這些設定的分級系統 GUID、允許未分級的遊戲旗標、目前系統下允許的最高評等識別碼、已拒絕的描述項集合。
-   WpcGameOverride (明確允許或拒絕每個應用程式識別碼的一個實例) 
    -   擁有 SID、應用程式識別碼識別遊戲、允許/拒絕狀態的屬性。

## <a name="data-representation-notes"></a>資料表示注意事項

架構中的數個設定受限於屬性為非 null 的 mof 檔案 \_ 。 這些不能設定為 null 變異。 針對所有非陣列類型，家長監護程式碼會初始化值。 若為數組，可以使用 null variant、empty variant 或大小為零的 variant 陣列來寫入空白狀態。 WMI 提供者會在讀取時將所有這些值正規化為 null 變異狀態表示。

## <a name="user-interface-extensibility-link-notes"></a>消費者介面擴充性連結注意事項

使用 WMI 註冊 UI 擴充性連結需要指定下列資訊：

-   GUID-如果是通用套件或套件的一部分，則多個連結可以共用相同的 GUID。
-   子系統-用於表示連結類型的分類，例如套件或獨立相容的應用程式
-   名稱資源 DLL 路徑和識別碼-指定要為連結顯示之顯示名稱的資源。
-   子標題資源 DLL 路徑和識別碼-指定資源，以取得名稱下方的其他文字。
-   影像路徑-24 ×24圖元點陣圖 (BMP) 的完整路徑，每圖元每圖元色深度，最好是 Alpha 色板。 這是以與 shell 擴充功能一致的方式來指定： <file system path> ， <negative resource ID> 。 例如： C： \\ Windows \\ System32 \\Wpccpl.dll，-20。
-   已停用的影像路徑-與上面的影像路徑相同，但顯示停用狀態的點陣圖變數除外。 當家長監護關閉時，就會顯示此影像。
-   Exe 路徑-要使用 ShellExecute () 叫用之可執行檔的完整路徑。 此路徑必須以反斜線指定，否則連結不會叫用可執行檔。 將% SID% 權杖新增至 exe 路徑之後，將會導致連結執行以 SID 字串取代目前正在查看其中樞頁面的使用者。 然後，可執行檔會使用 SID 字串來管理指定使用者的功能。

應用程式卸載必須移除擴充性連結註冊。

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Web 擴充性連結和 Web 內容篩選覆寫附注

藉由將 FilterID 屬性設定為與現有註冊的 UI 擴充性連結相同的 GUID，顯示的連結將會從其他設定中的一般連結升級至專屬的 Web 限制連結。 這是全電腦的設定，因此會導致內建的 Web 內容篩選 LSP 略過所有受控制使用者的篩選。 您也應該在 FilterName 屬性中設定描述性名稱，這個屬性是由資源 DLL 和識別碼的路徑所指定。

家長監護系統會從任何覆寫的網頁篩選器中建議下列內容：

-   接受使用者的整體家長監護開啟/關閉狀態。
-   接受使用者的活動報告設定。
-   監視 FilterID 屬性。 如果從廠商的指定 GUID 變更，其他篩選器就會取得擁有權，而廠商的篩選器應該停用它本身。 已加入 COM 介面，以降低定期檢查這項變更與 WMI 呼叫的額外負荷。
-   強烈建議您同時接受唯讀和讀取/寫入 HTTP 應用程式和 URL 豁免清單專案。
-   建議接受每位使用者的 URL 覆寫清單 (允許/封鎖清單) 。
-   很健全，可快速切換使用者。

家長監護不會限制 web 或其他內容篩選器如何插入 Windows 以進行篩選。 廠商可能會利用其目前的投資或慣用技術 (LSP、TDI、其他) 。

卸載廠商的篩選準則時，必須取消註冊 FilterID 和 FilterName 專案。 這是藉由將 FilterID 設定為 GUID \_ null，並將 FilterName 設定為 variant null 來執行。 然後會重新啟用內建的 web 內容篩選器。

請注意，重新啟用內建的網頁篩選器只會篩選新的會話，而不會篩選切換之前的作用中會話。

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Web 內容篩選允許/封鎖清單匯出/匯入格式

Windows 8 不支援這項功能。

**Windows 7 和 Windows Vista：** 支援這項功能。

&lt;WebAddresses&gt;

<URL AllowBlock="1">https://alloweddomain.com/&lt;/URL&gt;

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html&lt;/URL&gt;

<URL AllowBlock="2">https://blockeddomain.com/&lt;/URL&gt;

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html&lt;/URL&gt;

&lt;/WebAddresses&gt;

## <a name="application-restrictions-override-notes"></a>應用程式限制覆寫附注

應用程式限制覆寫是以每個使用者為基礎來設定，以允許特定的二進位檔或路徑。 如果已設定新的 parentally 控制使用者，且該使用者需要應用程式限制覆寫，建議將登錄中的 Windows 執行金鑰與標示為需要提高許可權的小型應用程式搭配使用，以寫入覆寫。 這將會產生一次性的認證提示，以設定使用者的覆寫，之後覆寫的目標二進位檔將不會對使用者造成干擾，因為會有進一步的系統管理員覆寫提示。

## <a name="actions-required-for-settings-changes-to-become-effective"></a>設定變更生效所需的動作

如果系統管理員變更已登入標準使用者的設定，則會產生警告訊息。 這表示在受控制的使用者登出後重新登入之前，設定變更可能不會生效。 這是保守的設計。 當受控制的使用者登入時，大部分的設定幾乎會立即生效。 其中一個例外狀況是遊戲，在下一次執行遊戲瀏覽器或叫用遊戲時，設定將會生效。

## <a name="sample-code"></a>範例程式碼

SDK 中提供的 c + + 範例會示範設定擴充功能的使用方式。 請參閱家長監護範例一節。

## <a name="independent-test-tools"></a>獨立測試工具

Wmimgmt.msc services.msc 外掛程式和 Wbemtest.exe 工具可促進類別和實例的檢查。

## <a name="64-bit-considerations"></a>64位考慮

64位 Windows 作業系統版本目前已安裝32位 WMI 提供者和64位提供者。

## <a name="general-code-development-and-debugging"></a>一般程式碼開發和偵錯工具

如果 Visual Studio 用於設定管理程式碼開發，本機的偵錯工具將需要以系統管理員許可權執行 Visual Studio， (使用命令列或右鍵選項) 叫用 [以系統管理員身分執行]。 這是由 UAC 所實行的進程和訊息隔離所致。

## <a name="minimum-compliance-api-settings-read"></a>設定讀取的最小合規性 API

### <a name="interfaces-and-methods"></a>介面和方法

標頭檔 Wpcapi 所控制的合規性 API 可使用 COM 介面，提供下列設定的簡化唯讀存取。

[**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) 根介面方法可讓您存取：

-   IWPCSettings 方法：
    -   IsLoggingRequired () -是否已為使用者將活動報告設定為 on？
    -   GetLastSettingsChangeTime () —應用程式可以知道是否有任何設定原則在先前的檢查之後變更。
    -   GetRestrictions () —閱讀 web 限制、時間限制、遊戲限制或應用程式限制是否設定為 on。
-   IWPCWebSettings 方法：
    -   GetSettings () –抓取或關閉篩選的旗標，並封鎖下載。
    -   RequestURLOverride () -將要求輸入至系統管理員覆寫 (過度使用的核准) 機制，以顯示包含要核准之 Url 的對話方塊。
-   IWPCGamesSettings 方法：
    -   IsBlocked () —針對指定的遊戲應用程式識別碼，這是由家長監護封鎖的遊戲，以及原因。
-   GetVisibility () ：提供是否目前隱藏家長監護 UI 的相關資訊。
-   GetWebFilterInfo () ：提供介面來取得目前使用中 Web 內容篩選器的識別碼。

### <a name="sample-code"></a>範例程式碼

SDK 中提供的 c + + 範例會示範如何使用合規性 API。 請參閱家長監護範例一節。

 

 



