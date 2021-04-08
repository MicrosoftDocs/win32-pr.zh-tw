---
title: 'Color2 屬性 (Shadow)  (VML) '
description: 'Color2 屬性 (Shadow)  (VML) '
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682831"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="eccfb-103">Color2 屬性 (Shadow)  (VML) </span><span class="sxs-lookup"><span data-stu-id="eccfb-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="eccfb-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="eccfb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eccfb-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="eccfb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eccfb-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="eccfb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eccfb-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="eccfb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eccfb-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="eccfb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eccfb-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="eccfb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eccfb-110">定義陰影的第二個色彩。</span><span class="sxs-lookup"><span data-stu-id="eccfb-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="eccfb-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eccfb-111">Read/write.</span></span> <span data-ttu-id="eccfb-112">**VgColor**。</span><span class="sxs-lookup"><span data-stu-id="eccfb-112">**VgColor**.</span></span>

<span data-ttu-id="eccfb-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="eccfb-113">**Applies To**</span></span>

[<span data-ttu-id="eccfb-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="eccfb-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="eccfb-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="eccfb-115">**Tag Syntax**</span></span>

<span data-ttu-id="eccfb-116"><v： *element* color2 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eccfb-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="eccfb-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="eccfb-117">**Script Syntax**</span></span>

<span data-ttu-id="eccfb-118"> color2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eccfb-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="eccfb-119">*運算式* =\*\* color2</span><span class="sxs-lookup"><span data-stu-id="eccfb-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="eccfb-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="eccfb-120">**Remarks**</span></span>

<span data-ttu-id="eccfb-121">使用第二種色彩來建立特殊的陰影效果。</span><span class="sxs-lookup"><span data-stu-id="eccfb-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="eccfb-122">如需第二個色彩的詳細資訊，請參閱 [Type](type-attribute--shadow--vml.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="eccfb-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="eccfb-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="eccfb-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="eccfb-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="eccfb-124">**Example**</span></span>

<span data-ttu-id="eccfb-125">陰影的第二個色彩有藍色。</span><span class="sxs-lookup"><span data-stu-id="eccfb-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 