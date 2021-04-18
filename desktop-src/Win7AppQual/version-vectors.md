---
description: 版本向量會處理 HTML 網頁中的條件式批註。 也就是說，版本向量可讓您根據瀏覽器版本建立標記。
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: 版本向量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321195"
---
# <a name="version-vectors"></a>版本向量

*版本向量* 會處理 HTML 網頁中的條件式批註。 也就是說，版本向量可讓您根據瀏覽器版本建立標記。

請考慮下列程式碼範例。


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



在此情況下，如果 Windows Internet Explorer 瀏覽器版本至少為5.5，則網頁上會顯示對應的段落。 雖然此範例中的第一個條件說明條件式批註的函式，但這些批註通常不會用來顯示第一個條件之類的標記。 相反地，上述範例中的其餘條件式批註更為常見。 在這些其餘的批註中，條件式批註會針對不同版本的瀏覽器使用不同的樣式表單。

上述程式碼範例也會檢查 Microsoft Internet Explorer 6 和 Windows Internet Explorer 7 是否相等。 但是針對 Windows Internet Explorer 8，此範例會使用 gte 運算子 (大於或等於) 。 這個運算子可協助您在未來進行此範例，以便在發行新版的瀏覽器時，使用樣式表單最符合標準的版本 (而不是使用錯誤的樣式表單或沒有樣式表單) 。 現有的應用程式通常不會考慮 Internet Explorer 過去 7 (的版本，或網站為) 建立的最新版本 Internet Explorer。 如需版本向量的詳細資訊，請參閱 MSDN Library 中的 [版本向量](/previous-versions/cc817577(v=msdn.10)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



