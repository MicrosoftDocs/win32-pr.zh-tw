---
title: VML 影子項目
description: VML 影子項目
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933278"
---
# <a name="vml-shadow-element"></a><span data-ttu-id="194d7-103">VML 影子項目</span><span class="sxs-lookup"><span data-stu-id="194d7-103">VML Shadow Element</span></span>

<span data-ttu-id="194d7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="194d7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="194d7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="194d7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="194d7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="194d7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="194d7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="194d7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="194d7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="194d7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="194d7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="194d7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="194d7-110">定義圖形的陰影。</span><span class="sxs-lookup"><span data-stu-id="194d7-110">Defines a shadow for a shape.</span></span>

<span data-ttu-id="194d7-111">下列屬性會修改陰影。</span><span class="sxs-lookup"><span data-stu-id="194d7-111">The following attributes modify a shadow.</span></span>



| <span data-ttu-id="194d7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="194d7-112">Attribute</span></span>                                          | <span data-ttu-id="194d7-113">描述</span><span class="sxs-lookup"><span data-stu-id="194d7-113">Description</span></span>                                        |
|----------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="194d7-114">色彩</span><span class="sxs-lookup"><span data-stu-id="194d7-114">Color</span></span>](color-attribute--shadow--vml.md)          | <span data-ttu-id="194d7-115">定義陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="194d7-115">Defines the color of a shadow.</span></span>                     |
| [<span data-ttu-id="194d7-116">Color2</span><span class="sxs-lookup"><span data-stu-id="194d7-116">Color2</span></span>](color2-attribute--shadow--vml.md)        | <span data-ttu-id="194d7-117">定義陰影的第二個色彩。</span><span class="sxs-lookup"><span data-stu-id="194d7-117">Defines the second color of a shadow.</span></span>              |
| [<span data-ttu-id="194d7-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="194d7-118">ID</span></span>](id-attribute--shadow--vml.md)                | <span data-ttu-id="194d7-119">指定陰影的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="194d7-119">Specifies the unique identifier of a shadow.</span></span>       |
| [<span data-ttu-id="194d7-120">矩陣</span><span class="sxs-lookup"><span data-stu-id="194d7-120">Matrix</span></span>](matrix-attribute--shadow--vml.md)        | <span data-ttu-id="194d7-121">定義陰影的觀點轉換。</span><span class="sxs-lookup"><span data-stu-id="194d7-121">Defines the perspective transform of a shadow.</span></span>     |
| [<span data-ttu-id="194d7-122">遮蔽</span><span class="sxs-lookup"><span data-stu-id="194d7-122">Obscured</span></span>](msdn-online-vml-obscured-attribute.md) | <span data-ttu-id="194d7-123">判斷陰影是否透明。</span><span class="sxs-lookup"><span data-stu-id="194d7-123">Determines whether the shadow is transparent.</span></span>      |
| [<span data-ttu-id="194d7-124">Offset</span><span class="sxs-lookup"><span data-stu-id="194d7-124">Offset</span></span>](offset-attribute--shadow--vml.md)        | <span data-ttu-id="194d7-125">定義陰影延伸超過圖形的距離。</span><span class="sxs-lookup"><span data-stu-id="194d7-125">Defines how far the shadow extends past the shape.</span></span> |
| [<span data-ttu-id="194d7-126">Offset2</span><span class="sxs-lookup"><span data-stu-id="194d7-126">Offset2</span></span>](msdn-online-vml-offset2-attribute.md)   | <span data-ttu-id="194d7-127">定義第二個位移。</span><span class="sxs-lookup"><span data-stu-id="194d7-127">Defines a second offset.</span></span>                           |
| [<span data-ttu-id="194d7-128">開啟</span><span class="sxs-lookup"><span data-stu-id="194d7-128">On</span></span>](on-attribute--shadow--vml.md)                | <span data-ttu-id="194d7-129">決定是否要顯示陰影。</span><span class="sxs-lookup"><span data-stu-id="194d7-129">Determines whether a shadow is displayed.</span></span>          |
| [<span data-ttu-id="194d7-130">不透明度</span><span class="sxs-lookup"><span data-stu-id="194d7-130">Opacity</span></span>](opacity-attribute--shadow--vml.md)      | <span data-ttu-id="194d7-131">決定陰影的透明度。</span><span class="sxs-lookup"><span data-stu-id="194d7-131">Determines the transparency of a shadow.</span></span>           |
| [<span data-ttu-id="194d7-132">起源</span><span class="sxs-lookup"><span data-stu-id="194d7-132">Origin</span></span>](origin-attribute--shadow--vml.md)        | <span data-ttu-id="194d7-133">定義陰影的中心。</span><span class="sxs-lookup"><span data-stu-id="194d7-133">Defines the center of the shadow.</span></span>                  |
| [<span data-ttu-id="194d7-134">型別</span><span class="sxs-lookup"><span data-stu-id="194d7-134">Type</span></span>](type-attribute--shadow--vml.md)            | <span data-ttu-id="194d7-135">指定陰影的類型。</span><span class="sxs-lookup"><span data-stu-id="194d7-135">Specifies the type of shadow.</span></span>                      |



 

<span data-ttu-id="194d7-136">**備註**</span><span class="sxs-lookup"><span data-stu-id="194d7-136">**Remarks**</span></span>

<span data-ttu-id="194d7-137">這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。</span><span class="sxs-lookup"><span data-stu-id="194d7-137">This element must be defined within a [Shape](shape-element--vml.md) element.</span></span>

<span data-ttu-id="194d7-138">此外， [On](on-attribute--shadow--vml.md) 屬性必須設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="194d7-138">In addition, the [On](on-attribute--shadow--vml.md) attribute must be set to **True**.</span></span>

<span data-ttu-id="194d7-139">以下是產生陰影所需的最少程式碼。</span><span class="sxs-lookup"><span data-stu-id="194d7-139">The following is the minimum code needed to produce a shadow.</span></span>


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



<span data-ttu-id="194d7-140">除非您增加 [位移](offset-attribute--shadow--vml.md) 值，否則您可能不會注意到陰影，因為預設位移是2pt，2pt。</span><span class="sxs-lookup"><span data-stu-id="194d7-140">You may not notice the shadow unless you increase the [Offset](offset-attribute--shadow--vml.md) values, since the default offset is 2pt,2pt.</span></span>

<span data-ttu-id="194d7-141">**範例**</span><span class="sxs-lookup"><span data-stu-id="194d7-141">**Examples**</span></span>

-   [<span data-ttu-id="194d7-142">簡單陰影範例</span><span class="sxs-lookup"><span data-stu-id="194d7-142">Simple Shadow Example</span></span>](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [<span data-ttu-id="194d7-143">動態陰影範例</span><span class="sxs-lookup"><span data-stu-id="194d7-143">Dynamic Shadow Example</span></span>](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 