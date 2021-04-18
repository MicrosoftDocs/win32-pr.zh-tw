---
title: 'On 屬性 (筆觸)  (VML) '
description: 'On 屬性 (筆觸)  (VML) '
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968914"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="0e8e6-103">On 屬性 (筆觸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="0e8e6-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="0e8e6-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0e8e6-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0e8e6-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0e8e6-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0e8e6-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0e8e6-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0e8e6-110">決定是否會顯示筆觸。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="0e8e6-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e8e6-111">Read/write.</span></span> <span data-ttu-id="0e8e6-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-112">**VgTriState**.</span></span>

<span data-ttu-id="0e8e6-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="0e8e6-113">**Applies To**</span></span>

[<span data-ttu-id="0e8e6-114">中風</span><span class="sxs-lookup"><span data-stu-id="0e8e6-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="0e8e6-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="0e8e6-115">**Tag Syntax**</span></span>

<span data-ttu-id="0e8e6-116"><v： *element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0e8e6-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="0e8e6-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="0e8e6-117">**Script Syntax**</span></span>

<span data-ttu-id="0e8e6-118">*element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0e8e6-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="0e8e6-119">*運算式* =*元素*。開啟</span><span class="sxs-lookup"><span data-stu-id="0e8e6-119">*expression*=*element*.on</span></span>

<span data-ttu-id="0e8e6-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="0e8e6-120">**Remarks**</span></span>

<span data-ttu-id="0e8e6-121">如果 **為 False**，則不會顯示筆觸。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="0e8e6-122">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-122">The default is **True**.</span></span>

<span data-ttu-id="0e8e6-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="0e8e6-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0e8e6-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="0e8e6-124">**Example**</span></span>

<span data-ttu-id="0e8e6-125">將不會顯示筆觸。</span><span class="sxs-lookup"><span data-stu-id="0e8e6-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 