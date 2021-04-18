---
title: VML 按鈕屬性
description: VML 按鈕屬性
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968707"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="58f8e-103">VML 按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="58f8e-103">VML Button Attribute</span></span>

<span data-ttu-id="58f8e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="58f8e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="58f8e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="58f8e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="58f8e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="58f8e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="58f8e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="58f8e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="58f8e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="58f8e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="58f8e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="58f8e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="58f8e-110">決定是否要將圖形視為按鈕處理。</span><span class="sxs-lookup"><span data-stu-id="58f8e-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="58f8e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58f8e-111">Read/write.</span></span> <span data-ttu-id="58f8e-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="58f8e-112">**VgTriState**.</span></span>

<span data-ttu-id="58f8e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="58f8e-113">**Applies To**</span></span>

[<span data-ttu-id="58f8e-114">形狀</span><span class="sxs-lookup"><span data-stu-id="58f8e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="58f8e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="58f8e-115">**Tag Syntax**</span></span>

<span data-ttu-id="58f8e-116"><v： *element* o:button = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="58f8e-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="58f8e-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="58f8e-117">**Remarks**</span></span>

<span data-ttu-id="58f8e-118">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="58f8e-118">The default is **False**.</span></span> <span data-ttu-id="58f8e-119">若為 **True**，則會以按鈕的形式處理圖形。</span><span class="sxs-lookup"><span data-stu-id="58f8e-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="58f8e-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="58f8e-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="58f8e-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="58f8e-121">**Example**</span></span>

<span data-ttu-id="58f8e-122">圖形是按鈕。</span><span class="sxs-lookup"><span data-stu-id="58f8e-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 