---
title: 從 Web Pages 呼叫 WDS
description: 您可以使用瀏覽器協助程式物件，從您建立或維護的任何網頁，呼叫 Microsoft Windows 桌面搜尋 (WDS)  (BHO) 和 Windows Internet Explorer。
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "104023148"
---
# <a name="calling-wds-from-web-pages"></a>從 Web Pages 呼叫 WDS

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

您可以使用瀏覽器協助程式物件，從您建立或維護的任何網頁，呼叫 Microsoft Windows 桌面搜尋 (WDS)  (BHO) 和 Windows Internet Explorer。 您可以在 MSN 網頁上查看其運作方式。 在上的搜尋方塊上方 https://www.msn.com 有數種搜尋類型： Web、新聞、影像、桌面、百科全書和 Local。 如果您按一下 [桌面]，會將搜尋參數傳遞至 Windows 桌面搜尋，以搜尋目錄並在 WDS 使用者介面中顯示結果。 若要讓使用者從您的網頁 (s) 啟動桌面搜尋，必須在其系統上安裝並啟用 WDSBHO、您的網頁 (s) 必須以 WDS 註冊為允許的 URL，而且您必須建立連結以將使用者 enetered 查詢傳遞至 WDS。

## <a name="enabling-the-wds-browser-help-object"></a>啟用 WDS 瀏覽器說明物件

當您安裝 WDS 時，預設會在 Internet Explorer 中安裝並啟用 BHO，但您可以輕鬆地確認它尚未停用或卸載。 在使用者的系統上，開啟 Internet Explorer，從 [**工具**] 功能表中選取 [**網際網路選項**]，按一下 [**程式**] 索引標籤，然後按一下 [**管理附加** 元件]。 在附加元件清單中，尋找 dsWebAllowBHO 類別，並確定已啟用。 停用 BHO 時，WDS 將繼續正常運作;不過，您將無法從網頁搜尋桌面。

以下兩個允許桌面搜尋的選項都將使用已註冊的搜尋應用程式，在本機執行搜尋。

## <a name="registering-web-page-urls"></a>註冊網頁 Url

登錄包含可從中呼叫 WDS 的「允許」網域 Url 清單。 若要將您的網頁 (的) ，您必須在登錄中列出您的網域 URL (s) 為 REG SZ，如下所示 \_ ：

**HKEY \_允許本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows 桌面搜尋** \\ **DSW** \\ \\*<number>* = <domainURL>

其中 **<number>** 是依序編號，而 **<domainURL>** 是您想要允許 WDS 搜尋的網頁 URL。 此 URL 字串可以 \* 在 URL 的開頭或結尾包含萬用字元星號。 例如，如果字串為 " \* . mydomain.com"，則您可以從和啟動 WDS 搜尋 https://www.mydomain.com https://mydomain.com 。

## <a name="enabling-desktop-search-by-url"></a>依 URL 啟用桌面搜尋

另一個不需要存取登錄的選項是在網頁上使用下列 URL (s) ：

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

其中 **QUERY** 是使用者正在搜尋的 URL 編碼字串，包括任何 [先進的查詢語法](-search-2x-wds-aqsreference.md) 字詞。

 

 




