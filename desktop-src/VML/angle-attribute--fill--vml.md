---
title: 'Angle 屬性 (填滿)  (的 VML) '
description: 'Angle 屬性 (填滿)  (的 VML) '
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024004"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="ee81d-103">Angle 屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="ee81d-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="ee81d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ee81d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ee81d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ee81d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ee81d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ee81d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ee81d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ee81d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ee81d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ee81d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ee81d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ee81d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ee81d-110">定義漸層填滿的角度。</span><span class="sxs-lookup"><span data-stu-id="ee81d-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="ee81d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ee81d-111">Read/write.</span></span> <span data-ttu-id="ee81d-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee81d-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="ee81d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ee81d-113">**Applies To**</span></span>

[<span data-ttu-id="ee81d-114">填滿</span><span class="sxs-lookup"><span data-stu-id="ee81d-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="ee81d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ee81d-115">**Tag Syntax**</span></span>

<span data-ttu-id="ee81d-116"><v： *element* angle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ee81d-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="ee81d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ee81d-117">**Script Syntax**</span></span>

<span data-ttu-id="ee81d-118">*element* . angle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ee81d-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="ee81d-119">*運算式* =*元素*. 角度</span><span class="sxs-lookup"><span data-stu-id="ee81d-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="ee81d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ee81d-120">**Remarks**</span></span>

<span data-ttu-id="ee81d-121">漸層的向量會與 blend 方向的向量（從某種色彩到另一種色彩）垂直。</span><span class="sxs-lookup"><span data-stu-id="ee81d-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="ee81d-122">預設值為 0 (零) 度，也就是由左至右的水準向量。</span><span class="sxs-lookup"><span data-stu-id="ee81d-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="ee81d-123">正面角度以逆時針方向旋轉漸層。</span><span class="sxs-lookup"><span data-stu-id="ee81d-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="ee81d-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ee81d-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ee81d-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="ee81d-125">**Example**</span></span>

<span data-ttu-id="ee81d-126">圖形的填滿是由兩個色彩的漸層所組成，在45度的角度從藍色到紅色。</span><span class="sxs-lookup"><span data-stu-id="ee81d-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="ee81d-127">左上角會顯示紅色，而藍色將會位於右下角。</span><span class="sxs-lookup"><span data-stu-id="ee81d-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 