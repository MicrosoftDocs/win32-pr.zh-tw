---
title: VML ShapeType 元素
description: VML ShapeType 元素
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186000"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="0aab5-103">VML ShapeType 元素</span><span class="sxs-lookup"><span data-stu-id="0aab5-103">VML ShapeType Element</span></span>

<span data-ttu-id="0aab5-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0aab5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0aab5-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0aab5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0aab5-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0aab5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0aab5-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0aab5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0aab5-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0aab5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0aab5-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0aab5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0aab5-110">定義可以用來建立其他圖形的圖形。</span><span class="sxs-lookup"><span data-stu-id="0aab5-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="0aab5-111">下列屬性會修改 **ShapeType**。</span><span class="sxs-lookup"><span data-stu-id="0aab5-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="0aab5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0aab5-112">Attribute</span></span>                                      | <span data-ttu-id="0aab5-113">描述</span><span class="sxs-lookup"><span data-stu-id="0aab5-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="0aab5-114">主機</span><span class="sxs-lookup"><span data-stu-id="0aab5-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="0aab5-115">判斷 **ShapeType** 是否為主要元素。</span><span class="sxs-lookup"><span data-stu-id="0aab5-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="0aab5-116">**備註**</span><span class="sxs-lookup"><span data-stu-id="0aab5-116">**Remarks**</span></span>

<span data-ttu-id="0aab5-117">**ShapeType** 與 **Shape** 元素相同，不同之處在于它無法參考另一個 **ShapeType** 元素。</span><span class="sxs-lookup"><span data-stu-id="0aab5-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="0aab5-118">當 **shape** 元素參考 **ShapeType** 時， **圖形** 可能會複製已在 **ShapeType** 中指定的部分屬性。</span><span class="sxs-lookup"><span data-stu-id="0aab5-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="0aab5-119">在這些情況下， **圖形** 中的屬性會覆寫 **ShapeType** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="0aab5-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="0aab5-120">**Type** 屬性不得與 **ShapeType** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0aab5-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="0aab5-121">CSS 定位屬性 (例如 **頂端**、**左方** 等 ) 不會從 **ShapeType** 傳遞給 **圖形**。</span><span class="sxs-lookup"><span data-stu-id="0aab5-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="0aab5-122">若要使用這個元素，請建立具有特定 [識別碼](id-attribute--vml.md)屬性的 **ShapeType** 。</span><span class="sxs-lookup"><span data-stu-id="0aab5-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="0aab5-123">然後建立一個 **圖形**，並以 **Type** 屬性參考 **ShapeType** 。</span><span class="sxs-lookup"><span data-stu-id="0aab5-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="0aab5-124">如需詳細資訊，請參閱 [Type](type-attribute--shape--vml.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0aab5-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 