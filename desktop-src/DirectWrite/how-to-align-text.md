---
title: 如何對齊文字
description: 您可以使用 IDWriteTextFormat 介面的 SetTextAlignment 方法來對齊 DirectWrite 文字。
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb765860f2fbaac94409aa9ec20c2269beb45cbb
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/31/2021
ms.locfileid: "106976307"
---
# <a name="how-to-align-text"></a><span data-ttu-id="ef052-103">如何對齊文字</span><span class="sxs-lookup"><span data-stu-id="ef052-103">How to Align Text</span></span>

<span data-ttu-id="ef052-104">您可以使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面的 [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)方法來對齊 [DirectWrite](direct-write-portal.md)文字，如下列將文字置中的程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="ef052-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



<span data-ttu-id="ef052-105">文字可以對齊版面配置方塊的開頭或尾端邊緣，也可以置中。</span><span class="sxs-lookup"><span data-stu-id="ef052-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="ef052-106">下圖顯示對齊設定為 [ [**DWRITE \_ 文字 \_ 對齊 \_ 開頭**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)]、[ [**DWRITE \_ 文字 \_ 對齊 \_ 中心**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)] 和 [ [**DWRITE \_ 文字 \_ 對齊的 \_ 尾端**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)] 的文字。</span><span class="sxs-lookup"><span data-stu-id="ef052-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![具有前置、置中和尾端對齊的文欄位落圖例](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="ef052-108">對齊取決於閱讀方向，以上是由左至右的讀取方向。</span><span class="sxs-lookup"><span data-stu-id="ef052-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="ef052-109">如果是由右至左的閱讀方向，則相反。</span><span class="sxs-lookup"><span data-stu-id="ef052-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="ef052-110">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件將會使用您在建立配置時所提供的 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)所指定的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="ef052-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="ef052-111">若要變更文字對齊，請使用 [**IDWriteTextLayout：： SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)。</span><span class="sxs-lookup"><span data-stu-id="ef052-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 
