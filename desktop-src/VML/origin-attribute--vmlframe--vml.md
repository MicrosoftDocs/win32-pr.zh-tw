---
title: '來源屬性 (VMLFrame)  (VML) '
description: '來源屬性 (VMLFrame)  (VML) '
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683030"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="dd9a7-103">來源屬性 (VMLFrame)  (VML) </span><span class="sxs-lookup"><span data-stu-id="dd9a7-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="dd9a7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dd9a7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dd9a7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dd9a7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dd9a7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dd9a7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dd9a7-110">定義框架裁剪區域的原點。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="dd9a7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dd9a7-111">Read/write.</span></span> <span data-ttu-id="dd9a7-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-112">**VgVector2D**.</span></span>

<span data-ttu-id="dd9a7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="dd9a7-113">**Applies To**</span></span>

[<span data-ttu-id="dd9a7-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="dd9a7-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="dd9a7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="dd9a7-115">**Tag Syntax**</span></span>

<span data-ttu-id="dd9a7-116"><v： *element* 原點 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="dd9a7-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="dd9a7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="dd9a7-117">**Script Syntax**</span></span>

<span data-ttu-id="dd9a7-118">*element* 。源 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="dd9a7-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="dd9a7-119">*運算式* =*元素*。來源</span><span class="sxs-lookup"><span data-stu-id="dd9a7-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="dd9a7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="dd9a7-120">**Remarks**</span></span>

<span data-ttu-id="dd9a7-121">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-121">The default value is 0,0.</span></span> <span data-ttu-id="dd9a7-122">請注意，只有當 [剪輯](msdn-online-vml-clip-attribute.md)為 **True** 時，**來源** 才適用。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="dd9a7-123">在這個屬性中，原點會定義為框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="dd9a7-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="dd9a7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="dd9a7-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="dd9a7-125">**Example**</span></span>

<span data-ttu-id="dd9a7-126">裁剪區域的來源為100pt、100pt。</span><span class="sxs-lookup"><span data-stu-id="dd9a7-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 