---
description: 某些應用程式會轉譯在工作區中繪製 (或移位) 物件。
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: 翻譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987817"
---
# <a name="translation"></a><span data-ttu-id="30397-103">翻譯</span><span class="sxs-lookup"><span data-stu-id="30397-103">Translation</span></span>

<span data-ttu-id="30397-104">某些應用程式會轉譯在工作區中繪製 (或移位) 物件。</span><span class="sxs-lookup"><span data-stu-id="30397-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="30397-105">藉由呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將適當的世界空間設定為頁面空間轉換。</span><span class="sxs-lookup"><span data-stu-id="30397-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="30397-106">SetWorldTransform 函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。</span><span class="sxs-lookup"><span data-stu-id="30397-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="30397-107">XFORM 的 eDx 和 eDy 成員會分別指定水準和垂直轉譯元件。</span><span class="sxs-lookup"><span data-stu-id="30397-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="30397-108">進行 *轉譯* 時，物件中的每個點都會依指定的量垂直、水準或同時移動。</span><span class="sxs-lookup"><span data-stu-id="30397-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="30397-109">下圖顯示從全局座標空間複製到頁面座標空間時，由10個單位轉譯為右邊的 20 x 單位矩形。</span><span class="sxs-lookup"><span data-stu-id="30397-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![圖例顯示在世界空間的某個位置，以及在頁面空間中不同位置的矩形](images/cstrn-09.png)

<span data-ttu-id="30397-111">在上圖中，矩形中每個點的 x 座標是大於原始 x 座標的10個單位。</span><span class="sxs-lookup"><span data-stu-id="30397-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="30397-112">水準轉譯可以用下列演算法來表示。</span><span class="sxs-lookup"><span data-stu-id="30397-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="30397-113">其中 x 是新的 x 座標，x 是原始 x 座標，而 Dx 是移動的水準距離。</span><span class="sxs-lookup"><span data-stu-id="30397-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="30397-114">垂直轉譯可以用下列演算法來表示。</span><span class="sxs-lookup"><span data-stu-id="30397-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="30397-115">其中 y ' 是新的 y 座標，y 是原始的 y 座標，而 Dy 是移動的垂直距離。</span><span class="sxs-lookup"><span data-stu-id="30397-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="30397-116">水準和垂直轉譯轉換可以使用三乘3的矩陣合併成單一作業。</span><span class="sxs-lookup"><span data-stu-id="30397-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="30397-117"> (矩陣乘法狀態的規則，其中一個矩陣的資料列數目必須等於另一個矩陣中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="30397-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="30397-118">矩陣 x y 1 中的整數 1 \| \| 是為了符合此需求而加入的預留位置。 ) </span><span class="sxs-lookup"><span data-stu-id="30397-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="30397-119">產生圖例轉譯轉換的三向3個矩陣包含下列值。</span><span class="sxs-lookup"><span data-stu-id="30397-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



