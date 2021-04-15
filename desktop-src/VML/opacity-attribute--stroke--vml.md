---
title: " (筆觸)  (VML) 的不透明度屬性"
description: " (筆觸)  (VML) 的不透明度屬性"
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463665"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="05a56-103"> (筆觸)  (VML) 的不透明度屬性</span><span class="sxs-lookup"><span data-stu-id="05a56-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="05a56-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="05a56-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="05a56-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="05a56-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="05a56-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="05a56-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="05a56-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="05a56-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="05a56-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="05a56-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="05a56-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="05a56-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="05a56-110">定義筆觸的透明度。</span><span class="sxs-lookup"><span data-stu-id="05a56-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="05a56-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="05a56-111">Read/write.</span></span> <span data-ttu-id="05a56-112">**VgFraction**。</span><span class="sxs-lookup"><span data-stu-id="05a56-112">**VgFraction**.</span></span>

<span data-ttu-id="05a56-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="05a56-113">**Applies To**</span></span>

[<span data-ttu-id="05a56-114">中風</span><span class="sxs-lookup"><span data-stu-id="05a56-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="05a56-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="05a56-115">**Tag Syntax**</span></span>

<span data-ttu-id="05a56-116"><v： *element* opacity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="05a56-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="05a56-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="05a56-117">**Script Syntax**</span></span>

<span data-ttu-id="05a56-118">*元素* 。不透明度 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="05a56-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="05a56-119">*運算式* =*元素*。不透明度</span><span class="sxs-lookup"><span data-stu-id="05a56-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="05a56-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="05a56-120">**Remarks**</span></span>

<span data-ttu-id="05a56-121">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="05a56-121">The default value is 1.0.</span></span>

<span data-ttu-id="05a56-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="05a56-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="05a56-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="05a56-123">**Example**</span></span>

<span data-ttu-id="05a56-124">筆劃為50% 透明。</span><span class="sxs-lookup"><span data-stu-id="05a56-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 