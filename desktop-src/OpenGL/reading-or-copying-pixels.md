---
title: 讀取或複製圖元
description: 您可以將畫面格緩衝區中的圖元讀取到記憶體中，以各種方式進行編碼，並使用 glReadPixels 將編碼的結果儲存在記憶體中。
ms.assetid: 6a6a710e-4d19-4fbf-9f25-abf22635c806
keywords:
- OpenGL 處理管線，讀取圖元
- OpenGL 處理管線，複製圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35600f3fb803d4453a24f9c5a051859ac159bad6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372016"
---
# <a name="reading-or-copying-pixels"></a><span data-ttu-id="e922c-105">讀取或複製圖元</span><span class="sxs-lookup"><span data-stu-id="e922c-105">Reading or Copying Pixels</span></span>

<span data-ttu-id="e922c-106">您可以將畫面格緩衝區中的圖元讀取到記憶體中，以各種方式進行編碼，並使用 [**glReadPixels**](glreadpixels.md)將編碼的結果儲存在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="e922c-106">You can read pixels from the framebuffer into memory, encode them in various ways, and store the encoded result in memory with [**glReadPixels**](glreadpixels.md).</span></span> <span data-ttu-id="e922c-107">此外，您可以使用 [**glCopyPixels**](glcopypixels.md)，將圖元值的矩形從畫面格緩衝區的一個區域複製到另一個區域。</span><span class="sxs-lookup"><span data-stu-id="e922c-107">In addition, you can copy a rectangle of pixel values from one region of the framebuffer to another with [**glCopyPixels**](glcopypixels.md).</span></span> <span data-ttu-id="e922c-108">函式 [**glReadBuffer**](glreadbuffer.md) 可控制讀取或複製圖元的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e922c-108">The function [**glReadBuffer**](glreadbuffer.md) controls which color buffer the pixels are read or copied from.</span></span>

 

 




