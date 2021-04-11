---
title: VML FillOK 屬性
description: VML FillOK 屬性
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316411"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="78f46-103">VML FillOK 屬性</span><span class="sxs-lookup"><span data-stu-id="78f46-103">VML FillOK Attribute</span></span>

<span data-ttu-id="78f46-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="78f46-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="78f46-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="78f46-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="78f46-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="78f46-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="78f46-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="78f46-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="78f46-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="78f46-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="78f46-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="78f46-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="78f46-110">決定是否會顯示填滿。</span><span class="sxs-lookup"><span data-stu-id="78f46-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="78f46-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="78f46-111">Read/write.</span></span> <span data-ttu-id="78f46-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="78f46-112">**VgTriState**.</span></span>

<span data-ttu-id="78f46-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="78f46-113">**Applies To**</span></span>

[<span data-ttu-id="78f46-114">路徑</span><span class="sxs-lookup"><span data-stu-id="78f46-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="78f46-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="78f46-115">**Tag Syntax**</span></span>

<span data-ttu-id="78f46-116"><v： *element* fillok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="78f46-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="78f46-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="78f46-117">**Script Syntax**</span></span>

<span data-ttu-id="78f46-118"> fillok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="78f46-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="78f46-119">*運算式* =\*\* fillok</span><span class="sxs-lookup"><span data-stu-id="78f46-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="78f46-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="78f46-120">**Remarks**</span></span>

<span data-ttu-id="78f46-121">如果 **為 False**，則表示路徑無法填入。</span><span class="sxs-lookup"><span data-stu-id="78f46-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="78f46-122">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="78f46-122">The default is **True**.</span></span> <span data-ttu-id="78f46-123">這個屬性會覆寫 parent 或 **fill** 元素中的所有其他填滿屬性。</span><span class="sxs-lookup"><span data-stu-id="78f46-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="78f46-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="78f46-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="78f46-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="78f46-125">**Example**</span></span>

<span data-ttu-id="78f46-126">將不會填入路徑。</span><span class="sxs-lookup"><span data-stu-id="78f46-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 