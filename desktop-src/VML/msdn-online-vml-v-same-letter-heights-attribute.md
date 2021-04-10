---
title: VML V 相同的字母高度屬性
description: VML V 相同的字母高度屬性
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682473"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="eed93-103">VML V 相同的字母高度屬性</span><span class="sxs-lookup"><span data-stu-id="eed93-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="eed93-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="eed93-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eed93-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="eed93-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eed93-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="eed93-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eed93-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="eed93-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eed93-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="eed93-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eed93-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="eed93-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eed93-110">判斷是否所有字母都會具有相同的高度，而不論初始案例為何。</span><span class="sxs-lookup"><span data-stu-id="eed93-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="eed93-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eed93-111">Read/write.</span></span> <span data-ttu-id="eed93-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="eed93-112">**VgTriState**.</span></span>

<span data-ttu-id="eed93-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="eed93-113">**Applies To**</span></span>

[<span data-ttu-id="eed93-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="eed93-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="eed93-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="eed93-115">**Tag Syntax**</span></span>

<span data-ttu-id="eed93-116"><v： *element* style = "v-相同的字母高度： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eed93-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="eed93-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="eed93-117">**Script Syntax**</span></span>

<span data-ttu-id="eed93-118"> node.js-相同的字母-高度 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eed93-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="eed93-119">*運算式* =\*\* node.js-相同的字母高度</span><span class="sxs-lookup"><span data-stu-id="eed93-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="eed93-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="eed93-120">**Remarks**</span></span>

<span data-ttu-id="eed93-121">若 **為 True**，則小寫字母會延伸至大寫字母的高度。</span><span class="sxs-lookup"><span data-stu-id="eed93-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="eed93-122">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="eed93-122">The default value is **False**.</span></span>

<span data-ttu-id="eed93-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="eed93-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="eed93-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="eed93-124">**Example**</span></span>

<span data-ttu-id="eed93-125">所有字母都會是相同的高度，而不會有任何大小寫。</span><span class="sxs-lookup"><span data-stu-id="eed93-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 