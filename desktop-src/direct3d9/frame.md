---
description: 定義座標框架或 &\# 0034; 參考的框架。 &\# 0034;框架範本是開啟的，而且可以包含任何物件。 載入框架實例時，D3DX 網格載入功能會將網格、FrameTransformMatrix 和框架範本實例辨識為子物件。
ms.assetid: vs|directx_sdk|~\frame.htm
title: " (Direct3D 9 圖形) 的框架"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77cc6f4618b3ded3afc9453c12a96b115ec4bfe0f90cb83a92826378212c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523031"
---
# <a name="frame-direct3d-9-graphics"></a> (Direct3D 9 圖形) 的框架

定義座標框架或「參考的框架」。 框架範本是開啟的，而且可以包含任何物件。 載入 **框架** 實例時，D3DX 網格載入功能會將 [**網格**](mesh.md)、 [**FrameTransformMatrix**](frametransformmatrix.md)和 **框架** 範本實例辨識為子物件。

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

框架範本可辨識框架內的子 **框架** 和 [**網格**](mesh.md) 節點，並可透過回呼函式辨識使用者定義的範本。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



