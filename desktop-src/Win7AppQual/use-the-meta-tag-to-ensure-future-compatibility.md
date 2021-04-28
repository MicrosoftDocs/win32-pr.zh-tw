---
description: 使用中繼標記以確保未來的相容性
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: 使用中繼標記以確保未來的相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a69180470c60dffc772f20fe6c515ba3803cbf2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084166"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>使用中繼標記以確保未來的相容性

Windows Internet Explorer 8 可讓您控制檔相容性模式，因此您可以指示瀏覽器以與舊版瀏覽器版本相同的方式轉譯網頁。 您也可以選擇何時更新網頁，但仍可繼續使用且正常運作。

## <a name="setting-the-meta-element"></a>設定中繼元素

**中繼** 元素包含 **內容** 屬性，可讓您指定在網頁中呈現內容的模式，如下表所示。



| 值 | 轉譯模式                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | 使用 Windows Internet Explorer 9 標準轉譯模式   |
| IE = 8  | 使用 Internet Explorer 8 標準轉譯模式           |
| IE = 7  | 使用 Windows Internet Explorer 7 標準轉譯模式   |
| IE = 5  | 使用 Microsoft Internet Explorer 5 標準轉譯模式 |



 

如需相容性和 X-UA 相容標頭的詳細資訊，請參閱 MSDN Library 中的 [定義檔相容性](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) 。

下列程式碼範例將示範如何強制網頁在 Internet Explorer 8 模式中呈現。


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>使用 HTTP 標頭

許多網站都包含數千 (或數萬個個別網頁的) ，因此在每個檔上設定 **中繼** 元素是不切實際的。 如果您想要設定所有頁面的 **中繼** 元素或資料夾所選取的頁面集合，您可以改為調整伺服器設定，並在 [HTTP 標頭](/previous-versions/cc817572(v=msdn.10))中新增 X-UA 相容的中繼資料。

針對相同伺服器上的頁面需要不同 **中繼** 元素值的網站，有數個工具會自動為您產生並插入適當的 **中繼** 元素。 例如，來自 Aggiorno 的 [ArtinSoft Web 工具](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) 公用程式會插入和移除 Internet Explorer 8 相容性標記功能，並可協助您的網站符合特定的相容性標準。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
