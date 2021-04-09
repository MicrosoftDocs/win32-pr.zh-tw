---
title: 使用 Background 元素
description: 使用 Background 元素
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- 網路研討會，背景元素
- 設計網頁、背景元素
- Vector Markup Language (VML) 、background 元素
- VML (Vector Markup Language) ，background 元素
- 向量圖形、背景元素
- background 元素
- VML 元素、背景
- VML 圖形、背景元素
- Vector Markup Language (VML) 自訂背景
- VML (Vector Markup Language) ，自訂背景
- 向量圖形，自訂背景
- VML 圖形，自訂背景
- 自訂背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842392"
---
# <a name="using-the-background-element"></a><span data-ttu-id="dd808-116">使用 Background 元素</span><span class="sxs-lookup"><span data-stu-id="dd808-116">Using the Background Element</span></span>

<span data-ttu-id="dd808-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="dd808-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dd808-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="dd808-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dd808-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="dd808-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dd808-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="dd808-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dd808-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="dd808-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dd808-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="dd808-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dd808-123">在本主題中，我們將說明如何使用 VML 中提供的元素自訂網頁的背景 `<background>` 。</span><span class="sxs-lookup"><span data-stu-id="dd808-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="dd808-124">如您從[ `<fill>` 使用](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)主題中學到的，您可以將子專案放在 `<fill>` `<shape>` 、 `<shapetype>` 或任何預先定義的 shape 元素內，以描述如何填滿圖形。</span><span class="sxs-lookup"><span data-stu-id="dd808-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="dd808-125">同樣地，您可以將 `<fill>` 子項目放在元素內， `<background>` 以描述如何填滿網頁的背景。</span><span class="sxs-lookup"><span data-stu-id="dd808-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="dd808-126">然後，您可以使用子項目的屬性屬性 `<fill>` 來自訂填滿效果，例如漸層 [填滿](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)、 [圖樣填滿](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)或 [圖片填滿](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)。</span><span class="sxs-lookup"><span data-stu-id="dd808-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="dd808-127">例如，若要繪製漸層填滿的背景，您可以在網頁的區域中輸入下列幾行 `<BODY>` ：</span><span class="sxs-lookup"><span data-stu-id="dd808-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="dd808-128">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858389) 。</span><span class="sxs-lookup"><span data-stu-id="dd808-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 