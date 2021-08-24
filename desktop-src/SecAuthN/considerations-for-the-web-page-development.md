---
description: Web 驗證訊息代理程式建置於 power Internet Explorer 的相同技術上 Windows。
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: 網頁開發的考量
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22932f40d5268059fc30e97817de0b3671cee7447974b038ea4be12eedd76ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883245"
---
# <a name="considerations-for-the-web-page-development"></a>網頁開發的考量

Web 驗證訊息代理程式建置於 power Internet Explorer 的相同技術上 Windows。 不過，由於此元件的特殊用途，Internet Explorer 的某些功能已停用或鎖定特定的設定。 此外，Web 驗證訊息代理程式也提供專用的事件記錄通道，以協助針對其處理的頁面問題進行疑難排解。

## <a name="internet-explorer-10-standard-document-mode"></a>Internet Explorer 10 標準檔案模式

Web 驗證訊息代理程式會顯示「IE10 標準模式」中的所有頁面。 您可以使用 Internet Explorer 中的開發人員工具，查看頁面在不同檔案模式下的運作方式。 如需 Internet Explorer 10 相容性的詳細資訊，請參閱[Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85))的 MSDN 主題。

## <a name="disabled-and-locked-down-features"></a>停用和鎖定功能

Internet Explorer 的數項功能完全停用，或鎖定為無法在作業系統的網際網路選項中變更的特定值。



| 功能                            | 狀態                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 應用程式快取 API ( "AppCache" )  | 已停用                                                                                                                                                                                                        |
| 連結歷程記錄                       | 已停用                                                                                                                                                                                                        |
| 暫存檔案                    | 啟用                                                                                                                                                                                                         |
| Cookie                            | 會話 cookie 已啟用。 允許保存的 cookie，但受限於自動清除，除非 Web 驗證訊息代理程式是在 SSO 模式中。 如需詳細資訊，請參閱「單一登入」一節。 |
| 索引資料庫                           | 已停用                                                                                                                                                                                                        |
| DOM 儲存體                        | 已停用                                                                                                                                                                                                        |
| ActiveX                            | 已停用                                                                                                                                                                                                        |
| 檔案下載                     | 已停用                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>HTTPS 需求

應用程式將用來與線上提供者通訊的第一個 URL 必須是 HTTPS。

## <a name="dimension-for-different-window-sizes"></a>不同視窗大小的維度

Windows 8 的應用程式可能會以數種不同的大小顯示，例如全螢幕、已調整大小的視窗，或像是共用快速鍵在內的快速鍵。 根據 Web 驗證訊息代理程式所顯示的視窗版面配置，網頁必須使用的大小可能會不同。 如需詳細資訊，請參閱 [調整成窄版面配置的指導方針](/previous-versions/windows/hh465371(v=win.10)) 和 [共用內容主題的指導方針](/previous-versions/windows/hh465251(v=win.10)) 。

網頁應該使用 CSS 媒體查詢來檢查它必須使用的大小，並據此加以配置。 不過，此頁面不應根據此處記載的確切圖元來設計，而且應該能夠調整成不同的大小。 本檔中指定的大小可能會在未來的作業系統版本中變更。

如果頁面無法容納分配空間中的所有資訊 (例如，應用程式要求的一長串許可權) ，Web 驗證代理人會提供捲軸，讓使用者視需要滾動頁面。 縮放功能也是由適用于桌上型電腦和膝上型電腦的縮放縮放裝置和 Ctrl + 滑鼠滾輪提供。

若要測試不同的縮放比例，請使用 Microsoft Visual Studio Professional 2012 中載入的[Web 驗證 Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)，以允許模擬全螢幕和調整大小的狀態。

除了上述的不同版面配置之外，請務必以不同的螢幕方向測試您的頁面 (例如，直向和橫向) ，以及不同的地區設定和語言，以及協助工具功能，例如 [讓所有專案變大] 選項開啟。

可用的版面配置如下：

-   [全螢幕](#full-screen)
-   [調整大小的視窗](#resized)
-   [快速鍵視圖](#charm-view)
-   [檔案選擇器視圖](#file-picker-view)

### <a name="full-screen"></a>全螢幕

針對全螢幕版面配置，網頁尺寸如下：

-   寬度：566圖元
-   高度：螢幕高度 (取決於螢幕解析度) 

下列範例會顯示全螢幕版面配置中的 web 驗證訊息代理程式 UI。

![全螢幕版面配置中的 web 驗證訊息代理程式 ui 範例](images/wab-figure2.png)

### <a name="resized"></a>調整

針對調整大小的視窗，網頁尺寸可以是：

-   寬度：260圖元
-   高度：螢幕高度 (取決於螢幕解析度) 

下列範例會在 XBox 網頁上的調整大小的視窗中，顯示 Web 驗證訊息代理程式 UI。 請注意，Web 驗證訊息代理程式 UI 只會在螢幕擷取畫面的右側。

![已調整大小之視窗中的 web 驗證訊息代理程式 ui 範例](images/wab-figure3.png)

### <a name="charm-view"></a>快速鍵視圖

針對快速鍵視圖，網頁尺寸如下：

-   寬度：566圖元
-   高度：螢幕高度 (取決於螢幕解析度) 

下列範例顯示 [快速鍵] 視圖中的 Web 驗證訊息代理程式 UI。

![範例顯示快速鍵 view 中的 web 驗證訊息代理程式 ui](images/wab-figure4.png)

### <a name="file-picker-view"></a>檔案選擇器視圖

針對檔案選擇器視圖，網頁尺寸如下：

-   寬度：566圖元
-   高度：螢幕高度 (取決於螢幕解析度) 

下列範例顯示 [檔案選擇器] 中的 [Web 驗證代理人] UI。

![範例顯示 [檔案選擇器] 視圖中的 web 驗證訊息代理程式 ui](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>預設沒有任何新視窗

依預設，沒有任何 Url 將會開啟新視窗，但是會顯示在 Web 驗證訊息代理程式視窗中。 這包括 window。開啟 JavaScript 方法、超連結的「目標」屬性，或當使用者使用 Ctrl + 按一下機制來強制開啟新視窗時。 這項規則的例外狀況是，當網頁在瀏覽器中宣告可安全流覽的連結時（如自訂超連結的目標所述）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
