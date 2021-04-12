---
title: VML ArrowOK 屬性
description: VML ArrowOK 屬性
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375772"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="37d13-103">VML ArrowOK 屬性</span><span class="sxs-lookup"><span data-stu-id="37d13-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="37d13-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="37d13-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="37d13-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="37d13-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="37d13-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="37d13-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="37d13-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="37d13-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="37d13-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="37d13-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="37d13-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="37d13-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="37d13-110">決定是否會顯示箭頭。</span><span class="sxs-lookup"><span data-stu-id="37d13-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="37d13-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37d13-111">Read/write.</span></span> <span data-ttu-id="37d13-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="37d13-112">**VgTriState**.</span></span>

<span data-ttu-id="37d13-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="37d13-113">**Applies To**</span></span>

[<span data-ttu-id="37d13-114">路徑</span><span class="sxs-lookup"><span data-stu-id="37d13-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="37d13-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="37d13-115">**Tag Syntax**</span></span>

<span data-ttu-id="37d13-116"><v： *element* arrowok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="37d13-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="37d13-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="37d13-117">**Script Syntax**</span></span>

<span data-ttu-id="37d13-118"> arrowok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="37d13-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="37d13-119">*運算式* =\*\* arrowok</span><span class="sxs-lookup"><span data-stu-id="37d13-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="37d13-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="37d13-120">**Remarks**</span></span>

<span data-ttu-id="37d13-121">如果 **為 False**，則路徑不會有箭頭。</span><span class="sxs-lookup"><span data-stu-id="37d13-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="37d13-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="37d13-122">The default is **False**.</span></span> <span data-ttu-id="37d13-123">這個屬性會覆寫父元素或 **筆劃** 元素中的所有其他箭頭屬性。</span><span class="sxs-lookup"><span data-stu-id="37d13-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="37d13-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="37d13-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="37d13-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="37d13-125">**Example**</span></span>

<span data-ttu-id="37d13-126">路徑不會有箭頭。</span><span class="sxs-lookup"><span data-stu-id="37d13-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 