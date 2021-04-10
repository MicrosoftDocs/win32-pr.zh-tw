---
title: 'On 屬性 (Shadow)  (VML) '
description: 'On 屬性 (Shadow)  (VML) '
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933447"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="8076f-103">On 屬性 (Shadow)  (VML) </span><span class="sxs-lookup"><span data-stu-id="8076f-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="8076f-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="8076f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8076f-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="8076f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8076f-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="8076f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8076f-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="8076f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8076f-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="8076f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8076f-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8076f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8076f-110">決定是否會顯示陰影。</span><span class="sxs-lookup"><span data-stu-id="8076f-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="8076f-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8076f-111">Read/write.</span></span> <span data-ttu-id="8076f-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="8076f-112">**VgTriState**.</span></span>

<span data-ttu-id="8076f-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="8076f-113">**Applies To**</span></span>

[<span data-ttu-id="8076f-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="8076f-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="8076f-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="8076f-115">**Tag Syntax**</span></span>

<span data-ttu-id="8076f-116"><v： *element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8076f-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="8076f-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="8076f-117">**Script Syntax**</span></span>

<span data-ttu-id="8076f-118">*element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8076f-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="8076f-119">*運算式* =*元素*。開啟</span><span class="sxs-lookup"><span data-stu-id="8076f-119">*expression*=*element*.on</span></span>

<span data-ttu-id="8076f-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="8076f-120">**Remarks**</span></span>

<span data-ttu-id="8076f-121">若 **為 True**，則會顯示陰影。</span><span class="sxs-lookup"><span data-stu-id="8076f-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="8076f-122">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="8076f-122">The default value is **False**.</span></span>

<span data-ttu-id="8076f-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="8076f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8076f-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="8076f-124">**Example**</span></span>

<span data-ttu-id="8076f-125">將會顯示陰影。</span><span class="sxs-lookup"><span data-stu-id="8076f-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 