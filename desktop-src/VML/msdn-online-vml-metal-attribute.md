---
title: VML 裸機屬性
description: VML 裸機屬性
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375393"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="4b98c-103">VML 裸機屬性</span><span class="sxs-lookup"><span data-stu-id="4b98c-103">VML Metal Attribute</span></span>

<span data-ttu-id="4b98c-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4b98c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4b98c-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4b98c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4b98c-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4b98c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4b98c-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4b98c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4b98c-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4b98c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4b98c-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4b98c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4b98c-110">判斷拉伸圖形的表面是否類似于金屬。</span><span class="sxs-lookup"><span data-stu-id="4b98c-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="4b98c-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4b98c-111">Read/write.</span></span> <span data-ttu-id="4b98c-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="4b98c-112">**VgTriState**.</span></span>

<span data-ttu-id="4b98c-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4b98c-113">**Applies To**</span></span>

[<span data-ttu-id="4b98c-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="4b98c-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="4b98c-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4b98c-115">**Tag Syntax**</span></span>

<span data-ttu-id="4b98c-116"><o： *element* 裸機 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4b98c-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="4b98c-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4b98c-117">**Script Syntax**</span></span>

<span data-ttu-id="4b98c-118">*元素* 。金屬 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4b98c-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="4b98c-119">*運算式* =*元素* 裸機</span><span class="sxs-lookup"><span data-stu-id="4b98c-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="4b98c-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4b98c-120">**Remarks**</span></span>

<span data-ttu-id="4b98c-121">如果設定為 **True**，這個屬性會使反射反映的光線變成材質色彩，而不是光線來源色彩，讓物件看起來更材質。若要進一步瞭解材質材質，specularity 必須相對高 (大約是 1.2) ，而 diffusity 相對較低 () 0.6。</span><span class="sxs-lookup"><span data-stu-id="4b98c-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="4b98c-122">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="4b98c-122">The default value is **False**.</span></span>

<span data-ttu-id="4b98c-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="4b98c-123">*Microsoft Office Extensions Attribute*</span></span>

 

 