---
description: 有些應用程式會提供一些功能，以反映在工作區中繪製的 (或鏡像) 物件。
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: 反射
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972549"
---
# <a name="reflection"></a><span data-ttu-id="157d5-103">反射</span><span class="sxs-lookup"><span data-stu-id="157d5-103">Reflection</span></span>

<span data-ttu-id="157d5-104">有些應用程式會提供一些功能，以反映在工作區中繪製的 (或鏡像) 物件。</span><span class="sxs-lookup"><span data-stu-id="157d5-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="157d5-105">包含反映功能的應用程式會使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將世界空間中的適當值設定為頁面空間轉換。</span><span class="sxs-lookup"><span data-stu-id="157d5-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="157d5-106">此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。</span><span class="sxs-lookup"><span data-stu-id="157d5-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="157d5-107">XFORM 的 eM11 和 eM22 成員分別指定水準和垂直反映元件。</span><span class="sxs-lookup"><span data-stu-id="157d5-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="157d5-108">*反映轉換* 會建立物件的鏡像影像（相對於 X 軸或 y 軸）。</span><span class="sxs-lookup"><span data-stu-id="157d5-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="157d5-109">簡單來說，反映只是負面調整。</span><span class="sxs-lookup"><span data-stu-id="157d5-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="157d5-110">若要產生水準反映，x 座標會乘以1。</span><span class="sxs-lookup"><span data-stu-id="157d5-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="157d5-111">若要產生垂直反映，y 座標會乘以1。</span><span class="sxs-lookup"><span data-stu-id="157d5-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="157d5-112">水準反映可透過下列演算法來表示：</span><span class="sxs-lookup"><span data-stu-id="157d5-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="157d5-113">其中 x 是 x 座標，x 是反映的結果。</span><span class="sxs-lookup"><span data-stu-id="157d5-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="157d5-114">產生水準反映的2到2個矩陣包含下列值：</span><span class="sxs-lookup"><span data-stu-id="157d5-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="157d5-115">垂直反映可透過下列演算法來表示：</span><span class="sxs-lookup"><span data-stu-id="157d5-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="157d5-116">其中 y 是 y 座標，y 是反映的結果。</span><span class="sxs-lookup"><span data-stu-id="157d5-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="157d5-117">產生垂直反映的2到2個矩陣包含下列值：</span><span class="sxs-lookup"><span data-stu-id="157d5-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="157d5-118">您可以使用下列2乘2矩陣，將水準反映和垂直反映作業合併為單一作業：</span><span class="sxs-lookup"><span data-stu-id="157d5-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 



