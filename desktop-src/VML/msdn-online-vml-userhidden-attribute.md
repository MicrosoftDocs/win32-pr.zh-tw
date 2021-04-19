---
title: VML UserHidden 屬性
description: VML UserHidden 屬性
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965431"
---
# <a name="vml-userhidden-attribute"></a><span data-ttu-id="fca62-103">VML UserHidden 屬性</span><span class="sxs-lookup"><span data-stu-id="fca62-103">VML UserHidden Attribute</span></span>

<span data-ttu-id="fca62-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="fca62-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fca62-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="fca62-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fca62-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="fca62-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fca62-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="fca62-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fca62-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="fca62-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fca62-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="fca62-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fca62-110">判斷是否隱藏腳本錨點。</span><span class="sxs-lookup"><span data-stu-id="fca62-110">Determines whether a script anchor is hidden.</span></span> <span data-ttu-id="fca62-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fca62-111">Read/write.</span></span> <span data-ttu-id="fca62-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="fca62-112">**VgTriState**.</span></span>

<span data-ttu-id="fca62-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="fca62-113">**Applies To**</span></span>

[<span data-ttu-id="fca62-114">形狀</span><span class="sxs-lookup"><span data-stu-id="fca62-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="fca62-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="fca62-115">**Tag Syntax**</span></span>

<span data-ttu-id="fca62-116"><v： *element* o:userhidden = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fca62-116"><v: *element* o:userhidden=" *expression* "></span></span>

<span data-ttu-id="fca62-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="fca62-117">**Remarks**</span></span>

<span data-ttu-id="fca62-118">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="fca62-118">The default is **False**.</span></span> <span data-ttu-id="fca62-119">若 **為 True**，即使圖形是可見的，腳本錨點仍會保持隱藏。</span><span class="sxs-lookup"><span data-stu-id="fca62-119">If **True**, script anchors stay hidden even if the shape is otherwise visible.</span></span>

<span data-ttu-id="fca62-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="fca62-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="fca62-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="fca62-121">**Example**</span></span>

<span data-ttu-id="fca62-122">圖形的腳本錨點是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="fca62-122">The script anchor of the shape is hidden.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 