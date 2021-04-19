---
title: VML RuleProxy 屬性
description: VML RuleProxy 屬性
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968115"
---
# <a name="vml-ruleproxy-attribute"></a><span data-ttu-id="49857-103">VML RuleProxy 屬性</span><span class="sxs-lookup"><span data-stu-id="49857-103">VML RuleProxy Attribute</span></span>

<span data-ttu-id="49857-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="49857-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49857-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="49857-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49857-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="49857-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49857-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="49857-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49857-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="49857-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49857-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="49857-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49857-110">判斷是否會使用規則引擎的 proxy。</span><span class="sxs-lookup"><span data-stu-id="49857-110">Determines whether a proxy for the rules engine will be used.</span></span> <span data-ttu-id="49857-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49857-111">Read/write.</span></span> <span data-ttu-id="49857-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="49857-112">**VgTriState**.</span></span>

<span data-ttu-id="49857-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="49857-113">**Applies To**</span></span>

[<span data-ttu-id="49857-114">形狀</span><span class="sxs-lookup"><span data-stu-id="49857-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="49857-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="49857-115">**Tag Syntax**</span></span>

<span data-ttu-id="49857-116"><v： *element* ruleproxy = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="49857-116"><v: *element* ruleproxy=" *expression* "></span></span>

<span data-ttu-id="49857-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="49857-117">**Remarks**</span></span>

<span data-ttu-id="49857-118">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="49857-118">The default value is **False**.</span></span> <span data-ttu-id="49857-119">若 **為 True**，則會使用 proxy。</span><span class="sxs-lookup"><span data-stu-id="49857-119">If **True**, a proxy is used.</span></span>

<span data-ttu-id="49857-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="49857-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="49857-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="49857-121">**Example**</span></span>

<span data-ttu-id="49857-122">Proxy 用來處理圖形。</span><span class="sxs-lookup"><span data-stu-id="49857-122">A proxy is used to process the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 