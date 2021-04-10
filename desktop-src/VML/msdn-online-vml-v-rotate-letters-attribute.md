---
title: VML V-旋轉字母屬性
description: VML V-旋轉字母屬性
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092766"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="5a386-103">VML V-旋轉字母屬性</span><span class="sxs-lookup"><span data-stu-id="5a386-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="5a386-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="5a386-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5a386-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="5a386-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5a386-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="5a386-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5a386-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="5a386-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5a386-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="5a386-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5a386-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="5a386-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5a386-110">決定是否旋轉文字的字母。</span><span class="sxs-lookup"><span data-stu-id="5a386-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="5a386-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5a386-111">Read/write.</span></span> <span data-ttu-id="5a386-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="5a386-112">**VgTriState**.</span></span>

<span data-ttu-id="5a386-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="5a386-113">**Applies To**</span></span>

[<span data-ttu-id="5a386-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="5a386-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5a386-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="5a386-115">**Tag Syntax**</span></span>

<span data-ttu-id="5a386-116"><v： *element* style = "v-旋轉字母： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5a386-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="5a386-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="5a386-117">**Script Syntax**</span></span>

<span data-ttu-id="5a386-118">*： v* -旋轉字母 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5a386-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="5a386-119">*運算式* =*： v*-旋轉字母</span><span class="sxs-lookup"><span data-stu-id="5a386-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="5a386-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="5a386-120">**Remarks**</span></span>

<span data-ttu-id="5a386-121">若 **為 True**，則文字的字母會旋轉90度。</span><span class="sxs-lookup"><span data-stu-id="5a386-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="5a386-122">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="5a386-122">The default value is **False**.</span></span>

<span data-ttu-id="5a386-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="5a386-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5a386-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="5a386-124">**Example**</span></span>

<span data-ttu-id="5a386-125">字母會旋轉90度。</span><span class="sxs-lookup"><span data-stu-id="5a386-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 