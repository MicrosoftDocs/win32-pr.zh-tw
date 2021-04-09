---
title: VML V-Text-Reverse 屬性
description: VML V-Text-Reverse 屬性
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023781"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="89e12-103">VML V-Text-Reverse 屬性</span><span class="sxs-lookup"><span data-stu-id="89e12-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="89e12-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="89e12-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="89e12-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="89e12-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="89e12-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="89e12-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="89e12-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="89e12-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="89e12-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="89e12-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="89e12-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="89e12-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="89e12-110">決定是否反轉資料列的版面配置順序。</span><span class="sxs-lookup"><span data-stu-id="89e12-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="89e12-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="89e12-111">Read/write.</span></span> <span data-ttu-id="89e12-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="89e12-112">**VgTriState**.</span></span>

<span data-ttu-id="89e12-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="89e12-113">**Applies To**</span></span>

[<span data-ttu-id="89e12-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="89e12-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="89e12-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="89e12-115">**Tag Syntax**</span></span>

<span data-ttu-id="89e12-116"><v： *element* style = "v-text-reverse： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="89e12-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="89e12-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="89e12-117">**Script Syntax**</span></span>

<span data-ttu-id="89e12-118">*element* 。 v-text-reverse = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="89e12-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="89e12-119">*運算式* =*元素*。 v-text-reverse</span><span class="sxs-lookup"><span data-stu-id="89e12-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="89e12-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="89e12-120">**Remarks**</span></span>

<span data-ttu-id="89e12-121">若 **為 True**，則會反轉資料列的版面配置順序。</span><span class="sxs-lookup"><span data-stu-id="89e12-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="89e12-122">這個屬性是用於垂直文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="89e12-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="89e12-123">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="89e12-123">The default value is **False**.</span></span>

<span data-ttu-id="89e12-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="89e12-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="89e12-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="89e12-125">**Example**</span></span>

<span data-ttu-id="89e12-126">版面配置順序相反。</span><span class="sxs-lookup"><span data-stu-id="89e12-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 