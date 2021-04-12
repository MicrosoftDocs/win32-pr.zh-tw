---
title: Windows 8.1 中的 Uri
description: Windows 8.1 只允許 HTTPs Uri，而非 HTTP Uri
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382545"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 只允許 HTTPs Uri，而非 HTTP Uri

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
伺服器-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

針對 Windows 8 所建立的應用程式可以在其應用程式內容 Uri 中包含 HTTP 和 HTTPs Uri，針對 Windows 8.1 所建立的應用程式可能只包含 HTTPs Uri。

唯一的例外是應用程式 AppxManifest.xml 檔中所指定的動態 ContentUriRules。 使用動態 ContentUriRules，應用程式可以存取系統管理員提供的其他網域或網路資源，例如群組原則的 Uri。 不過，只有在符合下列條件的情況下，Windows Store 應用程式才能使用動態 ContentUriRules：

-   群組原則已啟用
-   封裝指定了 enterpriseAuthentication 功能
-   封裝的 OSMaxVersionTested Windows 8.1 或更高

Windows 8.1 的新限制是增強式安全性限制的一部分，可進一步保護平臺。

## <a name="manifestations"></a>表現

在 Windows 8.1 上執行針對 Windows 8 所建立的應用程式時，允許在 [s](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) 中使用 HTTP uri。

## <a name="mitigations"></a>風險降低

我們建議 WWA 開發人員從 [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)) 的 (<[](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) x->--- 但是，如果您需要 AppCache、IndexedDB、地理位置或以程式設計方式存取剪貼簿存取的支援，您將需要繼續使用 <iframe> 適用于 Windows 8.1。

持續使用 <iframe> 針對遠端內容，應用程式的 s 中需要有新專案。 如果 web 內容需要叫用 s，則使用 web 內容的應用程式需要新的專案。請通知產生 [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) 事件。 如果您沒有 Visual Studio，可以藉由新增下列 XML 來更新應用程式資訊清單，包括子域的萬用字元 (例如 HTTPs:// \* . microsoft.com) ：


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>資源

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe> element \| <iframe> 物件](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Web 類型類別](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [ScriptNotify 事件](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 