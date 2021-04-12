---
description: 包含動畫設定的資料。
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025984"
---
# <a name="compressedanimationset"></a><span data-ttu-id="7d2ee-103">CompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="7d2ee-103">CompressedAnimationSet</span></span>

<span data-ttu-id="7d2ee-104">包含動畫設定的資料。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-104">Contains animation set data.</span></span>

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

<span data-ttu-id="7d2ee-105">其中：</span><span class="sxs-lookup"><span data-stu-id="7d2ee-105">Where:</span></span>

-   <span data-ttu-id="7d2ee-106">CompressedBlockSize-壓縮的主要畫面格動畫資料緩衝區中的壓縮資料大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="7d2ee-107">TicksPerSec：每秒發生的動畫主要畫面格刻度數目。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="7d2ee-108">PlaybackType-動畫集合播放迴圈的型別。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="7d2ee-109">請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="7d2ee-110">BufferLength-保存壓縮的主要畫面格動畫資料所需的最小緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="7d2ee-111">值等於 ( ( CompressedBlockSize + 3 ) /4 ) 。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="7d2ee-112">CompressedData \[ BufferLength \] -壓縮資料值的陣列。</span><span class="sxs-lookup"><span data-stu-id="7d2ee-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d2ee-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d2ee-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d2ee-114">範本</span><span class="sxs-lookup"><span data-stu-id="7d2ee-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="7d2ee-115">**XFILECOMPRESSEDANIMATIONSET**</span><span class="sxs-lookup"><span data-stu-id="7d2ee-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
