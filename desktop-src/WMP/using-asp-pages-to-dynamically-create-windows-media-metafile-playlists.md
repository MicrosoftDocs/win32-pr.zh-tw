---
title: 使用 ASP 頁面動態建立 Windows Media 中繼檔播放清單
description: 使用 ASP 頁面動態建立 Windows Media 中繼檔播放清單
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Media 中繼檔播放清單，建立
- 中繼檔播放清單，建立
- 播放清單，建立
- Windows Media 中繼檔播放清單，動態建立
- 中繼檔播放清單，動態建立
- 播放清單，動態建立
- Windows Media 中繼檔播放清單，ASP 頁面
- 中繼檔播放清單，ASP 頁面
- 播放清單，ASP 頁面
- 建立 Windows Media 中繼檔播放清單
- 動態建立 Windows Media 中繼檔播放清單
- ASP 網頁
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507181"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>使用 ASP 頁面動態建立 Windows Media 中繼檔播放清單

您可以使用 Active Server Pages (ASP 或 .asp 檔案) ，根據使用者提供的資訊動態產生播放清單。 ASP 頁面是一種動態網頁，用來搭配 Microsoft Internet Information Services (IIS) 。 ASP 是一種環境，可讓您合併 HTML、腳本和可重複使用的 ActiveX server 元件，以建立動態且功能強大的 Web 架構商務解決方案。 ASP 頁面為 IIS 啟用伺服器端腳本，提供 Microsoft Visual Basic Scripting Edition (VBScript) 和 Microsoft JScript 的原生支援。 本文假設您已熟悉 ASP 並定義變數。

所有的標頭資訊都必須包含在傳回給 Windows Media Player 的 ASP 頁面字串的第一行。

當您使用 ASP 頁面產生播放清單時，必須在 ASP 頁面中指定 **回應** 物件的 **ContentType** 和 **expires** 屬性的值，因為 Windows Media Player 的延遲問題。 **Response** 值必須是有效的 Windows Media 中繼檔副檔名。 可接受的值包括 wma、地板蠟、wmv、300k.wvx、asf 和 asx。

**Response** 屬性指定 Windows Media Player 快取播放清單檔案的時間長度（以秒為單位）。 將值指定為零會導致 Windows Media Player 在每次使用者重新整理頁面時，從伺服器要求新的播放清單。

請參閱 Platform SDK，以取得在 Active Server 頁面中使用 **回應** 物件的詳細資料。

下列程式碼是用來產生 Windows Media 中繼檔播放清單的 ASP 頁面範例。


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> </dl>

 

 




