---
title: VML PreferRelative 屬性
description: VML PreferRelative 屬性
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023570"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="ac659-103">VML PreferRelative 屬性</span><span class="sxs-lookup"><span data-stu-id="ac659-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="ac659-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ac659-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ac659-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ac659-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ac659-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ac659-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ac659-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ac659-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ac659-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ac659-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ac659-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ac659-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ac659-110">判斷在重新格式化之後是否儲存物件的原始大小。</span><span class="sxs-lookup"><span data-stu-id="ac659-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="ac659-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac659-111">Read/write.</span></span> <span data-ttu-id="ac659-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="ac659-112">**VgTriState**.</span></span>

<span data-ttu-id="ac659-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ac659-113">**Applies To**</span></span>

[<span data-ttu-id="ac659-114">形狀</span><span class="sxs-lookup"><span data-stu-id="ac659-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ac659-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ac659-115">**Tag Syntax**</span></span>

<span data-ttu-id="ac659-116"><v： *element* o:preferrelative = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ac659-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="ac659-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="ac659-117">**Remarks**</span></span>

<span data-ttu-id="ac659-118">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="ac659-118">The default is **False**.</span></span> <span data-ttu-id="ac659-119">若 **為 True**，將會儲存物件的原始大小，而且所有調整大小都會以該原始大小的百分比為基礎。</span><span class="sxs-lookup"><span data-stu-id="ac659-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="ac659-120">否則，每個調整大小都會將比例重設為100%。</span><span class="sxs-lookup"><span data-stu-id="ac659-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="ac659-121">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="ac659-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="ac659-122">**範例**</span><span class="sxs-lookup"><span data-stu-id="ac659-122">**Example**</span></span>

<span data-ttu-id="ac659-123">如果調整圖形的大小，則不會儲存原始的大小。</span><span class="sxs-lookup"><span data-stu-id="ac659-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 