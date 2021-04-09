---
title: 調整形狀
description: 調整形狀
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- 網路研討會，調整圖形
- 設計網頁、調整圖形
- Vector Markup Language (VML) 、縮放圖形
- VML (Vector Markup Language) 、縮放形狀
- 向量圖形，縮放形狀
- VML 圖形，縮放比例
- 調整形狀
- Vector Markup Language (VML) ，調整大小圖形
- VML (Vector Markup Language) ，調整大小圖形
- 向量圖形，調整大小圖形
- VML 圖形，調整大小
- 調整大小圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682517"
---
# <a name="scaling-shapes"></a><span data-ttu-id="da71b-115">調整形狀</span><span class="sxs-lookup"><span data-stu-id="da71b-115">Scaling Shapes</span></span>

<span data-ttu-id="da71b-116">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="da71b-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="da71b-117">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="da71b-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="da71b-118">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="da71b-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="da71b-119">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="da71b-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="da71b-120">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="da71b-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="da71b-121">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="da71b-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="da71b-122">您已瞭解如何使用 VML 在網頁上繪製和上色圖形。</span><span class="sxs-lookup"><span data-stu-id="da71b-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="da71b-123">在本主題中，我們將說明如何將圖形調整為任何您想要的大小。</span><span class="sxs-lookup"><span data-stu-id="da71b-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="da71b-124">VML 使用在[CSS2 規格](https://www.w3.org/TR/PR-CSS2/)的 [[視覺效果轉譯模型詳細資料](https://www.w3.org/TR/PR-CSS2/visudet.mdl)] 區段中定義的相同語法來指定包含方塊的大小，以便將圖形內容轉譯 (在包含的方塊中繪製) 。</span><span class="sxs-lookup"><span data-stu-id="da71b-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="da71b-125">您可以使用 [ **寬度** ] 和 [ **高度** ] 樣式屬性來定義包含方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="da71b-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="da71b-126">例如，如果您繪製 oval 並指定 **style**= ' width： 75pt; height： 100pt '，則會在包含大小為75點的方塊內繪製橢圓， (寬度) 100 點 (高度) ，如下列圖片所示：</span><span class="sxs-lookup"><span data-stu-id="da71b-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 個位元組) ](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="da71b-128">如果您將大小變更為 **style**= ' width： 120pt; height： 140pt '，則 oval 會變大，因為它會在新的包含方塊中調整120點大小， (寬度) 140 點 (高度) ，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="da71b-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 個位元組) ](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="da71b-130">如果您將大小變更為 **style**= ' width： 60pt; height： 40pt '，則 oval 會變得較小，因為它會在新的內含方塊中調整60點大小， (寬度) 40 點 (高度) ，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="da71b-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 個位元組) ](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 