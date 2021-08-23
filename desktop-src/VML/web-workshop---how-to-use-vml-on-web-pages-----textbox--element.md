---
title: 使用 Textbox 元素
description: 使用 Textbox 元素
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- 網路研討會、textbox 元素
- 設計網頁、textbox 元素
- Vector Markup Language (VML) 、textbox 元素
- '[VML (Vector Markup Language) ，textbox 元素'
- 向量圖形、textbox 元素
- textbox 元素
- VML 元素、textbox
- VML 圖形、textbox 元素
- Vector Markup Language (VML) 、附加文字
- VML (Vector Markup Language) ，附加文字
- 向量圖形，附加文字
- VML 圖形，附加文字
- 附加文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a9b4cb0b9096777a017dafd7df1c738621a4d5681ac3228741b3fd30386ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512621"
---
# <a name="using-the-textbox-element"></a>使用 Textbox 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

## <a name="examples"></a>範例：

若要將文字附加至矩形，您可以在網頁的區域中輸入下列幾行 `<BODY>` ：


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





若要將超連結附加至漸層填滿的圓角矩形，您可以在網頁的區域中輸入下列幾行 `<BODY>` ：

![textbox2.gif (1147 個位元組) ](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858397) 。

 

 