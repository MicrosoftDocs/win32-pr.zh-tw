---
title: 在服務工作窗格之間流覽
description: 在服務工作窗格之間流覽
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player 線上商店，導覽
- 線上商店，導覽
- 輸入2個線上商店，導覽
- Windows Media Player 線上商店、服務工作窗格
- 線上商店、服務工作窗格
- 輸入2個線上商店、服務工作窗格
- Windows Media Player 線上商店、工作窗格
- 線上商店、工作窗格
- 類型2線上商店、工作窗格
- 流覽類型2線上商店
- Windows Media Player，服務工作窗格
- Windows Media Player，工作窗格
- 服務工作窗格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f54a82f2637fe11b0a2a7703cc241c47e799999a89b56ba8ba19c079b7393de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647578"
---
# <a name="navigating-between-service-task-panes"></a>在服務工作窗格之間流覽

若要在 Windows Media Player 中的服務工作窗格之間流覽，您可以使用 **NavigateTaskPaneURL** 方法，此方法可透過使用 **external** 物件來使用。 當您使用這個方法時，您可以指定三個參數的值：

-   *bstrKeyName*。 這是線上商店的索引鍵名稱。 在線上商店中流覽時，請使用目前商店的金鑰名稱。
-   *bstrTaskPane*。 這個字串包含您想要流覽之服務工作窗格的名稱。
-   *bstrParams*。 這個字串包含您想要附加至您想要流覽之服務工作窗格所裝載網頁 URL 的查詢字串參數。

流覽是由您建立的網頁管理，稱為 [導覽] 頁面。 導覽頁面的 URL 是由 ServiceInfo 檔中的 **導覽** 元素所指定。 當您呼叫 **NavigateTaskPaneURL** 時，Windows Media Player 會開啟 [流覽] 頁面，而不是 **ServiceTask1**、 **ServiceTask2** 或 **ServiceTask3** 元素所指定的網頁。 它是接收 *bstrParams* 所指定之查詢字串的流覽頁面。 導覽頁面應該包含規則，這些規則可決定導覽之後，在服務工作窗格中顯示的內容。

例如，假設您想要讓使用者按一下連結，從 **ServiceTask1** 流覽至 **ServiceTask2**。 您可以使用下列 HTML 來建立連結：


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



當使用者按一下影片連結時，Windows Media Player 切換至 **ServiceTask2** 並開啟 [流覽] 頁面，並將下列查詢字串附加至其 URL。


```C++
?From=Music&To=2

```



From 參數會識別使用者按下連結的頁面，而 To 參數會識別他或她想要流覽的服務工作窗格數目。  (請注意，這些參數沒有任何特殊之處。 您可以使用任何您想要的參數做為您選擇的任何用途。 ) 

例如，下列範例程式碼顯示 ServiceInfo 檔中的 **導覽** 元素：


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



下列範例顯示產生的 URL （含查詢字串的完整）：


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



下列範例程式碼顯示導覽頁面：


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



上述程式碼只會建立 URL，並將瀏覽器重新導向至該 URL。 首先，程式碼會從 URL 查詢字串和查詢字串本身抓取值。 它會使用 To 參數的值來決定要顯示的頁面。 然後，它會將原始查詢字串附加至 URL。 最後，它會使用類似下列的 URL 來導覽瀏覽器：


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



當您以這種方式執行流覽時，請務必指定 [SelectedTaskPane](external-selectedtaskpane.md) ，以確定已反白顯示正確的工作按鈕。

-   **警告** 請小心使用查詢字串參數進行導覽。

任何建立 ASX 播放清單的人都可以提供 HTMLView 網頁。 這表示惡意網站可使用 **NavigateTaskPaneURL** 將查詢字串值傳遞至您的線上商店。 您必須規劃這種可能性，讓您的線上商店保持安全。 例如，如果您的線上商店只是向使用者顯示查詢字串值，惡意網站可能會顯示未預期的文字。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**導覽元素**](navigate-element.md)
</dt> <dt>

[**類型2線上商店的流覽**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




