---
description: 將點陣圖複製到平行四邊形中;使用 PlgBlt 函式，此函式會執行從來源裝置內容中的矩形到目的地裝置內容中之平行四邊形的位區塊傳輸。
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: 點陣圖旋轉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991283"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="b0a43-103">點陣圖旋轉</span><span class="sxs-lookup"><span data-stu-id="b0a43-103">Bitmap Rotation</span></span>

<span data-ttu-id="b0a43-104">將點陣圖複製到平行四邊形中;使用 [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) 函式，此函式會執行從來源裝置內容中的矩形到目的地裝置內容中之平行四邊形的位區塊傳輸。</span><span class="sxs-lookup"><span data-stu-id="b0a43-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="b0a43-105">若要旋轉點陣圖，應用程式必須提供座標（以全球單位），以用於平行四邊形的角落。</span><span class="sxs-lookup"><span data-stu-id="b0a43-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="b0a43-106"> (如需旋轉和世界單位的詳細資訊，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="b0a43-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 



