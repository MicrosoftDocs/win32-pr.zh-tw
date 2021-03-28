---
description: 五個世界對頁轉換可以合併成單一的 3 x 3 矩陣。
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: 結合的世界到頁面空間轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972737"
---
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="a2603-103">結合的世界到頁面空間轉換</span><span class="sxs-lookup"><span data-stu-id="a2603-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="a2603-104">五個世界對頁轉換可以合併成單一的 3 x 3 矩陣。</span><span class="sxs-lookup"><span data-stu-id="a2603-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="a2603-105">[**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)函式可用來將兩個世界空間與頁面空間的轉換結合在一起。</span><span class="sxs-lookup"><span data-stu-id="a2603-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="a2603-106">結合的轉換可用來改變與特定裝置內容相關聯的輸出 (DC) ，方法是呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，並提供此矩陣的元素。</span><span class="sxs-lookup"><span data-stu-id="a2603-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="a2603-107">當應用程式呼叫 **SetWorldTransform** 時，它會將 3 x 3 矩陣的元素儲存在 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a2603-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="a2603-108">此結構的成員對應至 3 x 3 矩陣的前兩個數據行;矩陣的最後一個資料行不是必要的，因為它的值是常數。</span><span class="sxs-lookup"><span data-stu-id="a2603-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="a2603-109">您可以藉由呼叫 [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) 函式並提供指向 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，來恢復目前世界轉換矩陣的元素。</span><span class="sxs-lookup"><span data-stu-id="a2603-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



