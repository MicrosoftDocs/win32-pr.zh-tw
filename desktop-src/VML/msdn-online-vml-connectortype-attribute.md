---
title: VML ConnectorType 屬性
description: VML ConnectorType 屬性
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965650"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="90bd4-103">VML ConnectorType 屬性</span><span class="sxs-lookup"><span data-stu-id="90bd4-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="90bd4-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="90bd4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="90bd4-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="90bd4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="90bd4-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="90bd4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="90bd4-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="90bd4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="90bd4-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="90bd4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="90bd4-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="90bd4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="90bd4-110">表示用於聯結圖形的連接器類型。</span><span class="sxs-lookup"><span data-stu-id="90bd4-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="90bd4-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="90bd4-111">Read/write.</span></span> <span data-ttu-id="90bd4-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="90bd4-112">**String**.</span></span>

<span data-ttu-id="90bd4-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="90bd4-113">**Applies To**</span></span>

[<span data-ttu-id="90bd4-114">形狀</span><span class="sxs-lookup"><span data-stu-id="90bd4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="90bd4-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="90bd4-115">**Tag Syntax**</span></span>

<span data-ttu-id="90bd4-116"><v： *element* o:connectortype = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="90bd4-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="90bd4-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="90bd4-117">**Remarks**</span></span>

<span data-ttu-id="90bd4-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="90bd4-118">Values include:</span></span>



| <span data-ttu-id="90bd4-119">值</span><span class="sxs-lookup"><span data-stu-id="90bd4-119">Value</span></span>    | <span data-ttu-id="90bd4-120">描述</span><span class="sxs-lookup"><span data-stu-id="90bd4-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="90bd4-121">無</span><span class="sxs-lookup"><span data-stu-id="90bd4-121">none</span></span>     | <span data-ttu-id="90bd4-122">沒有連接器。</span><span class="sxs-lookup"><span data-stu-id="90bd4-122">No connector.</span></span>                  |
| <span data-ttu-id="90bd4-123">直</span><span class="sxs-lookup"><span data-stu-id="90bd4-123">straight</span></span> | <span data-ttu-id="90bd4-124">預設值。</span><span class="sxs-lookup"><span data-stu-id="90bd4-124">Default.</span></span> <span data-ttu-id="90bd4-125">直接連接器。</span><span class="sxs-lookup"><span data-stu-id="90bd4-125">A straight connector.</span></span> |
| <span data-ttu-id="90bd4-126">肘</span><span class="sxs-lookup"><span data-stu-id="90bd4-126">elbow</span></span>    | <span data-ttu-id="90bd4-127">肘形接點。</span><span class="sxs-lookup"><span data-stu-id="90bd4-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="90bd4-128">彎曲</span><span class="sxs-lookup"><span data-stu-id="90bd4-128">curved</span></span>   | <span data-ttu-id="90bd4-129">彎曲的接點。</span><span class="sxs-lookup"><span data-stu-id="90bd4-129">A curved connector.</span></span>            |



 

<span data-ttu-id="90bd4-130">圖形化編輯器的規則引擎也可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="90bd4-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="90bd4-131">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="90bd4-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="90bd4-132">**範例**</span><span class="sxs-lookup"><span data-stu-id="90bd4-132">**Example**</span></span>

<span data-ttu-id="90bd4-133">圖形會使用直線作為接點。</span><span class="sxs-lookup"><span data-stu-id="90bd4-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 