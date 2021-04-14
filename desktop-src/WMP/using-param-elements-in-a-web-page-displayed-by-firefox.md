---
title: 在 Firefox 所顯示的網頁中使用 PARAM 元素
description: 在 Firefox 所顯示的網頁中使用 PARAM 元素
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player，OBJECT 元素中的 PARAM 元素
- Windows Media Player 物件模型、OBJECT 元素中的 PARAM 元素
- 物件模型、OBJECT 元素中的 PARAM 專案
- Windows Media Player Mobile、OBJECT 元素中的 PARAM 元素
- Windows Media Player ActiveX 控制項、OBJECT 元素中的 PARAM 元素
- Windows Media Player 行動 ActiveX 控制項、OBJECT 元素中的 PARAM 元素
- ActiveX 控制項、OBJECT 元素中的 PARAM 元素
- 內嵌、網頁
- 物件元素中的網頁內嵌、PARAM 元素
- OBJECT 元素中的 PARAM 元素
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media Player Mobile、Firefox
- Windows Media Player ActiveX 控制項，Firefox
- Windows Media Player Mobile ActiveX 控制項，Firefox
- ActiveX 控制項、Firefox
- Firefox、OBJECT 元素中的 PARAM 元素
- 網頁內嵌、Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311679"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="4c027-122">在 Firefox 所顯示的網頁中使用 PARAM 元素</span><span class="sxs-lookup"><span data-stu-id="4c027-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="4c027-123">您可以使用物件專案內的 PARAM 專案來設定播放機控制項的初始狀態。</span><span class="sxs-lookup"><span data-stu-id="4c027-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="4c027-124">例如，下列範例中的 PARAM 元素會指定控制項應該自動播放西雅圖 .wmv。</span><span class="sxs-lookup"><span data-stu-id="4c027-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="4c027-125">大部分的 PARAM 元素都可以由 Internet Explorer 和 Firefox 來解讀。</span><span class="sxs-lookup"><span data-stu-id="4c027-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="4c027-126">不過，Firefox 外掛程式不支援一些 PARAM 元素。</span><span class="sxs-lookup"><span data-stu-id="4c027-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="4c027-127">如需 Firefox 外掛程式支援哪些 PARAM 元素的詳細資訊，請參閱 [OBJECT 元素中的 param](param-elements-in-an-object-element.md)專案。</span><span class="sxs-lookup"><span data-stu-id="4c027-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c027-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c027-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c027-129">**搭配 Firefox 使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="4c027-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




