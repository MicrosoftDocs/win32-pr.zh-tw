---
title: 如何對齊文字
description: 您可以使用 IDWriteTextFormat 介面的 SetTextAlignment 方法來對齊 DirectWrite 文字。
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650361"
---
# <a name="how-to-align-text"></a>如何對齊文字

您可以使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面的 [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)方法來對齊 [DirectWrite](direct-write-portal.md)的文字，如下列將文字置中的程式碼所示。


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



文字可以對齊版面配置方塊的開頭或尾端邊緣，也可以置中。 下圖顯示對齊設定為 [ [**DWRITE \_ 文字 \_ 對齊 \_ 開頭**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)]、[ [**DWRITE \_ 文字 \_ 對齊 \_ 中心**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)] 和 [ [**DWRITE \_ 文字 \_ 對齊的 \_ 尾端**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)] 的文字。

![具有前置、置中和尾端對齊的文欄位落圖例](images/textalignment.png)

> [!Note]  
> 對齊取決於閱讀方向，以上是由左至右的讀取方向。 如果是由右至左的閱讀方向，則相反。

 

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件將會使用您在建立配置時所提供的 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)所指定的對齊方式。 若要變更文字對齊，請使用 [**IDWriteTextLayout：： SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)。

 

 
