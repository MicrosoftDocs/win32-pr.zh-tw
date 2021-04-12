---
title: VML Font-Family 屬性
description: VML Font-Family 屬性
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024070"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="7eb47-103">VML Font-Family 屬性</span><span class="sxs-lookup"><span data-stu-id="7eb47-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="7eb47-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7eb47-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7eb47-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7eb47-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7eb47-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7eb47-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7eb47-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7eb47-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7eb47-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7eb47-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7eb47-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7eb47-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7eb47-110">定義 textpath 字型的系列。</span><span class="sxs-lookup"><span data-stu-id="7eb47-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="7eb47-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7eb47-111">Read/write.</span></span> <span data-ttu-id="7eb47-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="7eb47-112">**String**.</span></span>

<span data-ttu-id="7eb47-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7eb47-113">**Applies To**</span></span>

[<span data-ttu-id="7eb47-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="7eb47-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="7eb47-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7eb47-115">**Tag Syntax**</span></span>

<span data-ttu-id="7eb47-116"><v： *element* style = "font-family： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7eb47-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="7eb47-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="7eb47-117">**Script Syntax**</span></span>

<span data-ttu-id="7eb47-118"> fontfamily = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7eb47-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="7eb47-119">*運算式* =\*\* fontfamily</span><span class="sxs-lookup"><span data-stu-id="7eb47-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="7eb47-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="7eb47-120">**Remarks**</span></span>

<span data-ttu-id="7eb47-121">定義字型名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb47-121">Defines the font name.</span></span> <span data-ttu-id="7eb47-122">您可以使用或泛型型別（例如 Arial、sans-serif、草書、幻想或等體），來使用特定的名稱，例如 Arial。</span><span class="sxs-lookup"><span data-stu-id="7eb47-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="7eb47-123">這些值與標準 HTML 樣式屬性相同。</span><span class="sxs-lookup"><span data-stu-id="7eb47-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="7eb47-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="7eb47-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="7eb47-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="7eb47-125">**Example**</span></span>

<span data-ttu-id="7eb47-126">文字的字型家族為 Arial。</span><span class="sxs-lookup"><span data-stu-id="7eb47-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 