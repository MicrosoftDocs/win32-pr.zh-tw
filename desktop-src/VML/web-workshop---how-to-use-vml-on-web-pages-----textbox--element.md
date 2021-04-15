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
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463648"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="ec72e-116">使用 Textbox 元素</span><span class="sxs-lookup"><span data-stu-id="ec72e-116">Using the Textbox Element</span></span>

<span data-ttu-id="ec72e-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ec72e-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec72e-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ec72e-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec72e-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ec72e-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec72e-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ec72e-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec72e-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ec72e-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec72e-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ec72e-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="ec72e-123">範例：</span><span class="sxs-lookup"><span data-stu-id="ec72e-123">Examples:</span></span>

<span data-ttu-id="ec72e-124">若要將文字附加至矩形，您可以在網頁的區域中輸入下列幾行 `<BODY>` ：</span><span class="sxs-lookup"><span data-stu-id="ec72e-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="ec72e-125">若要將超連結附加至漸層填滿的圓角矩形，您可以在網頁的區域中輸入下列幾行 `<BODY>` ：</span><span class="sxs-lookup"><span data-stu-id="ec72e-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

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





<span data-ttu-id="ec72e-127">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858397) 。</span><span class="sxs-lookup"><span data-stu-id="ec72e-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 