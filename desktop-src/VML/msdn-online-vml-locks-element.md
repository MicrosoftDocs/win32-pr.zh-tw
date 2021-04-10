---
title: VML 鎖定元素
description: VML 鎖定元素
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a3d246e486d1b7db99484777355b9160b71b6b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092932"
---
# <a name="vml-locks-element"></a><span data-ttu-id="bece1-103">VML 鎖定元素</span><span class="sxs-lookup"><span data-stu-id="bece1-103">VML Locks Element</span></span>

<span data-ttu-id="bece1-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="bece1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bece1-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="bece1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bece1-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="bece1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bece1-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="bece1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bece1-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="bece1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bece1-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="bece1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bece1-110">定義圖形的鎖定。</span><span class="sxs-lookup"><span data-stu-id="bece1-110">Defines a lock for a shape.</span></span>

<span data-ttu-id="bece1-111">下列屬性會修改鎖定。</span><span class="sxs-lookup"><span data-stu-id="bece1-111">The following attributes modify a lock.</span></span>



| <span data-ttu-id="bece1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="bece1-112">Attribute</span></span>                                                    | <span data-ttu-id="bece1-113">描述</span><span class="sxs-lookup"><span data-stu-id="bece1-113">Description</span></span>                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="bece1-114">AdjustHandles</span><span class="sxs-lookup"><span data-stu-id="bece1-114">AdjustHandles</span></span>](msdn-online-vml-adjusthandles-attribute.md) | <span data-ttu-id="bece1-115">決定是否可以編輯圖形的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bece1-115">Determines whether the handles of a shape can be edited.</span></span>                    |
| [<span data-ttu-id="bece1-116">AspectRatio</span><span class="sxs-lookup"><span data-stu-id="bece1-116">AspectRatio</span></span>](msdn-online-vml-aspectratio-attribute.md)     | <span data-ttu-id="bece1-117">決定是否可以透過編輯器來變更圖形的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="bece1-117">Determines whether the aspect ratio of a shape can be changed by an editor.</span></span> |
| [<span data-ttu-id="bece1-118">裁剪</span><span class="sxs-lookup"><span data-stu-id="bece1-118">Cropping</span></span>](msdn-online-vml-cropping-attribute.md)           | <span data-ttu-id="bece1-119">決定是否允許在編輯器中進行裁剪。</span><span class="sxs-lookup"><span data-stu-id="bece1-119">Determines whether cropping will be allowed in an editor.</span></span>                   |
| [<span data-ttu-id="bece1-120">內線</span><span class="sxs-lookup"><span data-stu-id="bece1-120">Ext</span></span>](ext-attribute--lock--vml.md)                          | <span data-ttu-id="bece1-121">定義圖形化編輯器鎖定動作的行為。</span><span class="sxs-lookup"><span data-stu-id="bece1-121">Defines the behavior of locking actions for a graphical editor.</span></span>             |
| [<span data-ttu-id="bece1-122">分組</span><span class="sxs-lookup"><span data-stu-id="bece1-122">Grouping</span></span>](msdn-online-vml-grouping-attribute.md)           | <span data-ttu-id="bece1-123">決定是否可以將圖形分組在編輯器中。</span><span class="sxs-lookup"><span data-stu-id="bece1-123">Determines whether shapes can be grouped in an editor.</span></span>                      |
| [<span data-ttu-id="bece1-124">位置</span><span class="sxs-lookup"><span data-stu-id="bece1-124">Position</span></span>](position-attribute--lock--vml.md)                | <span data-ttu-id="bece1-125">決定是否在編輯器中鎖定圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="bece1-125">Determines whether the position of a shape is locked in an editor.</span></span>          |
| [<span data-ttu-id="bece1-126">旋轉</span><span class="sxs-lookup"><span data-stu-id="bece1-126">Rotation</span></span>](rotation-attribute--lock--vml.md)                | <span data-ttu-id="bece1-127">決定是否允許在編輯器中旋轉形狀。</span><span class="sxs-lookup"><span data-stu-id="bece1-127">Determines whether rotation of shapes will be allowed in an editor.</span></span>         |
| [<span data-ttu-id="bece1-128">選取範圍</span><span class="sxs-lookup"><span data-stu-id="bece1-128">Selection</span></span>](msdn-online-vml-selection-attribute.md)         | <span data-ttu-id="bece1-129">決定是否可在編輯器中選取圖形。</span><span class="sxs-lookup"><span data-stu-id="bece1-129">Determines whether the shape is selectable in an editor.</span></span>                    |
| [<span data-ttu-id="bece1-130">ShapeType</span><span class="sxs-lookup"><span data-stu-id="bece1-130">ShapeType</span></span>](msdn-online-vml-shapetype-attribute.md)         | <span data-ttu-id="bece1-131">判斷自選圖形類型是否可由編輯器變更。</span><span class="sxs-lookup"><span data-stu-id="bece1-131">Determines whether the AutoShapes type can be changed by an editor.</span></span>         |
| [<span data-ttu-id="bece1-132">Text</span><span class="sxs-lookup"><span data-stu-id="bece1-132">Text</span></span>](msdn-online-vml-text-attribute.md)                   | <span data-ttu-id="bece1-133">決定是否可以編輯附加至圖形的文字。</span><span class="sxs-lookup"><span data-stu-id="bece1-133">Determines whether the text attached to a shape can be edited.</span></span>              |
| [<span data-ttu-id="bece1-134">頂點</span><span class="sxs-lookup"><span data-stu-id="bece1-134">Vertices</span></span>](msdn-online-vml-vertices-attribute.md)           | <span data-ttu-id="bece1-135">決定是否可以透過編輯器變更路徑的頂點。</span><span class="sxs-lookup"><span data-stu-id="bece1-135">Determines whether the vertices of a path can be changed by an editor.</span></span>      |



 

<span data-ttu-id="bece1-136">**備註**</span><span class="sxs-lookup"><span data-stu-id="bece1-136">**Remarks**</span></span>

<span data-ttu-id="bece1-137">這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。</span><span class="sxs-lookup"><span data-stu-id="bece1-137">This element must be defined within a [Shape](shape-element--vml.md) element.</span></span>

<span data-ttu-id="bece1-138">**鎖定** 元素是 VML 的 Microsoft Office 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="bece1-138">The **Locks** element is a Microsoft Office Extension to VML.</span></span>

 

 