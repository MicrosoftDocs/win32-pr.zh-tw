---
title: VML BlackLevel 屬性
description: VML BlackLevel 屬性
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023687"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="3f9ef-103">VML BlackLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="3f9ef-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="3f9ef-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f9ef-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f9ef-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f9ef-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f9ef-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f9ef-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f9ef-110">定義影像中的黑色濃度。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="3f9ef-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3f9ef-111">Read/write.</span></span> <span data-ttu-id="3f9ef-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-112">**VgNumber**.</span></span>

<span data-ttu-id="3f9ef-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="3f9ef-113">**Applies To**</span></span>

[<span data-ttu-id="3f9ef-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="3f9ef-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="3f9ef-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="3f9ef-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f9ef-116"><v： *element* blacklevel = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3f9ef-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="3f9ef-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="3f9ef-117">**Script Syntax**</span></span>

<span data-ttu-id="3f9ef-118"> blacklevel = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3f9ef-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="3f9ef-119">*運算式* =\*\* blacklevel</span><span class="sxs-lookup"><span data-stu-id="3f9ef-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="3f9ef-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="3f9ef-120">**Remarks**</span></span>

<span data-ttu-id="3f9ef-121">允許修改色彩層級，讓黑色顯示為 true 黑色，而其他所有色彩則會顯示為黑色以上的陰影。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="3f9ef-122">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-122">The default value is 0.</span></span> <span data-ttu-id="3f9ef-123">雖然允許正和負無限大之間的任何數位，但小於-0.5 的值會顯示為所有的黑色，而大於0.5 的值會顯示為全部白色。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="3f9ef-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="3f9ef-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f9ef-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="3f9ef-125">**Example**</span></span>

<span data-ttu-id="3f9ef-126">影像將會顯示為非常深的色調。</span><span class="sxs-lookup"><span data-stu-id="3f9ef-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 