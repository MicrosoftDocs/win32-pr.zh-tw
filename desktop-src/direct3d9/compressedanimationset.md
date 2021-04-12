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
# <a name="compressedanimationset"></a>CompressedAnimationSet

包含動畫設定的資料。

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

其中：

-   CompressedBlockSize-壓縮的主要畫面格動畫資料緩衝區中的壓縮資料大小總計（以位元組為單位）。
-   TicksPerSec：每秒發生的動畫主要畫面格刻度數目。
-   PlaybackType-動畫集合播放迴圈的型別。 請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。
-   BufferLength-保存壓縮的主要畫面格動畫資料所需的最小緩衝區大小（以位元組為單位）。 值等於 ( ( CompressedBlockSize + 3 ) /4 ) 。
-   CompressedData \[ BufferLength \] -壓縮資料值的陣列。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**XFILECOMPRESSEDANIMATIONSET**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
