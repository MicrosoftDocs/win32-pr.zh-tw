---
description: 下表描述 Microsoft Internet Explorer 6 和 Windows Internet Explorer 8 之間的變更。
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: IE 8 瀏覽器變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c775448d8eca55097b0121592c28ece0b2c347f4492e7a48b2d51d9ab688fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680287"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>附錄1： Internet Explorer 6 至 Internet Explorer 8 瀏覽器變更

下表描述 Microsoft Internet Explorer 6 和 Windows Internet Explorer 8 之間的變更。



設計從 Internet Explorer 6 到 Internet Explorer 7 的變更

將 Internet Explorer 7 的變更設計為 Internet Explorer 8

$ {ROWSPAN2} $Internet Explorer 版本控制 $ {REMOVE} $  

檢查是否有不正確的程式碼 Internet Explorer 6、Windows Internet Explorer 7，或透過[使用者代理字串探查、版本向量或條件式批註](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))Internet Explorer 8。

-   當長時間的使用者代理程式 (UA) 字串遇到只接受較短 UA 字串的伺服器時，使用者會看到 [錯誤頁面](https://www.enhanceie.com/ua.aspx)。

<!-- -->

-   Internet Explorer 8 中的相容性檢視預設為內部網路網站開啟，會傳送 Internet Explorer 7 的使用者代理程式字串。 若要區分 Internet Explorer 7 和相容性檢視，請尋找新的 [Trident token](/archive/blogs/ie/)。

$ {ROWSPAN3} $ 標準合規性更新

-   適用于 [指定的檔案模式](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85))。
-   針對內部網路網站， [Internet Explorer 8 相容性檢視模式](/archive/blogs/ie/)預設為開啟，通常會將[Internet Explorer 7 的標準更新還原到 Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8)。
-   使用 [EmulateIE7 X-UA 相容](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) 的 HTTP 標頭或 **中繼** 元素，啟用網站或特定網頁上的相容性檢視。

$ {REMOVE} $  

不相關模式例外狀況：您不需要將 [標準合規性] DOCTYPE 參數設定為 [關閉] ) ，就能針對指定 [不相容模式] DOCTYPE (的網頁進行標準合規性變更。

適用于 Internet Explorer 7 標準或「Strict」模式和更新版本：

-   原始程式碼第一行中的[XML 初構](/previous-versions/windows/internet-explorer/ie-developer/)不會再造成 DOCTYPE 宣告失敗。
-   方塊[模型](/previous-versions/windows/internet-explorer/ie-developer/)溢位內容相交方塊，且不再自動擴大 box div 以符合內容。
-   [某些 CSS 篩選](/previous-versions/windows/internet-explorer/ie-developer/) (例如， \* HTML、 \_ 底線及/ \* \* /批註) 不受支援。
-   只會具現化[嵌套物件中最外層的物件元素](/previous-versions/windows/internet-explorer/ie-developer/)。
-   [依賴 select 元素](/previous-versions/windows/internet-explorer/ie-developer/) 來取得 HWND 以搭配 Microsoft Win32 api 使用的應用程式可能會中斷，因為 [SELECT 元素](/archive/blogs/ie/) 現在是無視窗控制項。
-   不支援[ (CDF) 的通道定義格式](/previous-versions/aa740486(v=msdn.10))，以支援 RSS 摘要。
-   [XBM](/previous-versions/aa740486(v=msdn.10))是一種專為 X 型系統設計的影像處理格式，不受支援。
-   不允許前端檔以外的[基底標記](/previous-versions/aa740486(v=msdn.10))。

適用于 Internet Explorer 8 標準模式和更新版本：

-   當元素後面接著 [**資料表**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx)、[**表單**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx)、 [**NOFRAMES**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)或 [**NOSCRIPT**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx)專案時，會自動關閉未 [封閉的 P](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx)專案。
-   不支援[格式不正確的 HTML](/archive/blogs/ie/site-compatibility-and-ie8) ，而是採用格式正確且有效的標記。
-   不支援 ["className" 屬性](/archive/blogs/ie/site-compatibility-and-ie8) 語法，而是以 "class" 語法為優先。
-   [attributes 集合](/archive/blogs/ie/site-compatibility-and-ie8)未包含 Windows Internet Explorer 可辨識的所有可能屬性。
-   [屬性排序已變更](/archive/blogs/ie/site-compatibility-and-ie8)，會影響屬性集合、InnerHTML 和 outerHTML。
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) 區分大小寫，且不會搜尋名稱屬性。
-   [一般 CSS 前置詞選取器](/archive/blogs/ie/site-compatibility-and-ie8) (也就是 v \\ ： \* 語法) ，而不支援明確的標記名稱。
-   不支援[css 運算式](/archive/blogs/ie/site-compatibility-and-ie8)，以利改善 css 支援或 DHTML 邏輯。
-   適用于自訂 JSON 物件方法的程式碼可能會與 Internet Explorer 8 中 [新的原生 JSON 物件](/archive/blogs/ie/site-compatibility-and-ie8) 發生衝突。
-   取消設定 currentStyle 物件上的[初始屬性](/archive/blogs/ie/site-compatibility-and-ie8)會傳回它們的初始值。
-   currentStyle 物件樣式物件上[未指定的屬性值](/archive/blogs/ie/site-compatibility-and-ie8)會傳回空字串 (例如，請參閱[ASP.NET 功能表和 IE8 轉譯白色問題](/archive/blogs/giorgio/)blog 文章) 。

<!-- -->

-   針對協助工具有問題的網站和應用程式，請 [在所有 Internet Explorer 轉譯模式中更新 ARIA 語法](/archive/blogs/ie/)。
-   檢查 [從 Internet Explorer 6 到 Internet Explorer 8 的 CSS 更新完整清單](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx)。

安全性改善

-   無論檔案模式為何，都適用。
-   您可以使用 [群組原則](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab)來關閉安全性功能。

<!-- -->

-   [開啟工具](/previous-versions/aa740486(v=msdn.10))略過視窗。不允許關閉提示。
-   預設會啟用物件快取[保護](/previous-versions/windows/internet-explorer/ie-developer/)，這會在使用者流覽至新網域時封鎖對物件參考的存取， (套用至 Windows XP Service Pack 2 (SP2) 和更新版本) 上的 Internet Explorer 6 和更新版本。
-   [DHTML 程式碼片段](/previous-versions/windows/internet-explorer/ie-developer/) 預設為停用。
-   會封鎖[寫入狀態列的腳本](/previous-versions/windows/internet-explorer/ie-developer/)。
-   如果 Url 不符合 RFC 指導方針，[建立 url 可能會失敗](/previous-versions/windows/internet-explorer/ie-developer/)。
-   如果網站設定為僅 SSLv2，或網站安全性憑證已過期或無效、發生錯誤或具有弱式加密，則[HTTPS 頁面會顯示錯誤頁面](/previous-versions/windows/internet-explorer/ie-developer/)。
-   僅支援 ["Punycode" 編碼的國際化功能變數名稱](/previous-versions/windows/internet-explorer/ie-developer/) 。 系統會封鎖其他格式，例如 ANSI 和 UTF-8。
-   會封鎖[跨網域腳本 url](/previous-versions/windows/internet-explorer/ie-developer/)、DOM 物件中的重新導向導覽和框架導覽。
-   從腳本建立的強制回應[或非強制回應對話方塊](/previous-versions/aa740486(v=msdn.10))看起來可能[稍微大](/archive/blogs/ie/)一點。
-   不[安全的通訊協定](/previous-versions/aa740486(v=msdn.10))視圖-來源、在 WinINET 層級的 Gopher () ，且 Telnet 無法運作。

<!-- -->

-   [XSS 篩選器](/archive/blogs/ie/) 預設為開啟，除非您透過 X-XSS 保護 HTTP 標頭停用，否則會封鎖最常發生于類型 1 xss 攻擊的腳本模式。
-   不支援跨網域、跨檔通訊的攻擊（例如 [腳本 SRC](/archive/blogs/jscript/) ），以提供更安全的 [XDM 和 XDR AJAX 功能](/archive/blogs/ie/)。
-   [手動操作 URL 雜湊的](/previous-versions//cc891506(v=vs.85))啟用 AJAX 的網站可能會被新的視窗所中斷。
-   [新的 AJAX 功能](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) （例如 [XDM](/archive/blogs/ie/) ）具有 [**原生屬性**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) ，可能會與現有的自訂屬性發生衝突。
-   檔案[上傳控制項](/archive/blogs/ie/)只會將檔案路徑（而不是完整路徑）提交到伺服器。
-   以「 [影像/」 \* MIME 類型](/archive/blogs/ie/) 傳遞的 HTML 程式碼或腳本已封鎖而無法執行。
-   在不同的安全性內容中[流覽最上層的框架](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85))至網站，會開啟新的視窗或索引標籤，而不是在現有的框架內流覽。
-   [utf-7 編碼的腳本](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85))會強制進入 Windows-1252 編碼，這可能會導致純文字呈現。
-   [HTTP/HTTPS 「混合模式」頁面](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) 會顯示一個對話方塊，預設為僅顯示安全專案 (與先前的非安全預設) 。 使用者可能會誤 [選擇封鎖 HTTP 元素](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0)，例如金鑰影像。
-   [DEP/NX 預設為開啟](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx)，它會封鎖某些附加元件 (也就是，使用舊版 ATL 建立的 ActiveX 控制項和 COM) 物件，不會在記憶體中標示為「無法執行的可執行檔」的程式碼執行。
-   如果未建立 SSL 通道以回應源伺服器的連接要求，則會封鎖[web proxy 所傳回的內容](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85))。

架構變更

-   不論檔或相容性模式都適用。

<!-- -->

-   針對[網際網路、內部網路和限制的網站區域，](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85))預設會啟用[受保護模式](/previous-versions/windows/internet-explorer/ie-developer/)。 此模式[會封鎖可能造成安全性風險的瀏覽器延伸模組，使其無法從執行](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85))和[較低許可權的應用程式存取更高許可權的進程](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85))，例如 [開始] 功能表、主控台和 Microsoft Windows registry (適用于 Internet Explorer Vista 和更新版本 Windows) 7 和更新版本。

<!-- -->

-   [受保護模式更新](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85))：內部網路會在中型 (中執行，而不是預設的低) 完整性層級。
-   [鬆散結合的 Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie)可能會封鎖附加元件 (亦即 ActiveX 控制項和 COM 物件，) 執行下列其中一項動作：
    -   使用 windows 階層技術來找出 UI 框架和索引標籤 windows (，這些視窗現在會在不同的完整性層級) 的不同進程中執行。
    -   從低完整性的索引標籤程式，建立 UI 框架的子類別 (現在是) 的整合層級。
    -   在 UI 框架與索引標籤之間使用不支援的訊息技術。



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在遷移至 Internet Explorer 8 時解決應用程式相容性問題](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
