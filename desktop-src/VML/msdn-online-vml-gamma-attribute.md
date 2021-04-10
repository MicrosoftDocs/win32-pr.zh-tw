---
title: VML Gamma 屬性
description: VML Gamma 屬性
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092935"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="ee661-103">VML Gamma 屬性</span><span class="sxs-lookup"><span data-stu-id="ee661-103">VML Gamma Attribute</span></span>

<span data-ttu-id="ee661-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ee661-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ee661-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ee661-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ee661-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ee661-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ee661-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ee661-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ee661-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ee661-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ee661-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ee661-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ee661-110">定義影像的對比量。</span><span class="sxs-lookup"><span data-stu-id="ee661-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="ee661-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ee661-111">Read/write.</span></span> <span data-ttu-id="ee661-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="ee661-112">**VgNumber**.</span></span>

<span data-ttu-id="ee661-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ee661-113">**Applies To**</span></span>

[<span data-ttu-id="ee661-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="ee661-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="ee661-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ee661-115">**Tag Syntax**</span></span>

<span data-ttu-id="ee661-116"><v： *element* gamma = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ee661-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="ee661-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ee661-117">**Script Syntax**</span></span>

<span data-ttu-id="ee661-118">*element* 。 gamma = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ee661-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="ee661-119">*運算式* =*元素* gamma</span><span class="sxs-lookup"><span data-stu-id="ee661-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="ee661-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ee661-120">**Remarks**</span></span>

<span data-ttu-id="ee661-121">減少小於1的 gamma 會修改影像，使其更 contrasty，而大於1的值則會減少對比。</span><span class="sxs-lookup"><span data-stu-id="ee661-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="ee661-122">有用的值是從0.3 到大約3。</span><span class="sxs-lookup"><span data-stu-id="ee661-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="ee661-123">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="ee661-123">The default value is 0.</span></span>

<span data-ttu-id="ee661-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ee661-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ee661-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="ee661-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 