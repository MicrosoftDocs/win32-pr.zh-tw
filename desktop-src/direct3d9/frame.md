---
description: 定義座標框架或 &\# 0034; 參考的框架。 &\# 0034;框架範本是開啟的，而且可以包含任何物件。 載入框架實例時，D3DX 網格載入功能會將網格、FrameTransformMatrix 和框架範本實例辨識為子物件。
ms.assetid: vs|directx_sdk|~\frame.htm
title: " (Direct3D 9 圖形) 的框架"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845968"
---
# <a name="frame-direct3d-9-graphics"></a><span data-ttu-id="18ed8-104"> (Direct3D 9 圖形) 的框架</span><span class="sxs-lookup"><span data-stu-id="18ed8-104">Frame (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="18ed8-105">定義座標框架或「參考的框架」。</span><span class="sxs-lookup"><span data-stu-id="18ed8-105">Defines a coordinate frame, or "frame of reference."</span></span> <span data-ttu-id="18ed8-106">框架範本是開啟的，而且可以包含任何物件。</span><span class="sxs-lookup"><span data-stu-id="18ed8-106">The Frame template is open and can contain any object.</span></span> <span data-ttu-id="18ed8-107">載入 **框架** 實例時，D3DX 網格載入功能會將 [**網格**](mesh.md)、 [**FrameTransformMatrix**](frametransformmatrix.md)和 **框架** 範本實例辨識為子物件。</span><span class="sxs-lookup"><span data-stu-id="18ed8-107">The D3DX mesh-loading functions recognize [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md), and **Frame** template instances as child objects when loading a **Frame** instance.</span></span>

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

<span data-ttu-id="18ed8-108">框架範本可辨識框架內的子 **框架** 和 [**網格**](mesh.md) 節點，並可透過回呼函式辨識使用者定義的範本。</span><span class="sxs-lookup"><span data-stu-id="18ed8-108">The frame template recognizes child **Frame** and [**Mesh**](mesh.md) nodes inside a frame and can recognize user-defined templates through a callback function.</span></span>

## <a name="see-also"></a><span data-ttu-id="18ed8-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18ed8-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ed8-110">範本</span><span class="sxs-lookup"><span data-stu-id="18ed8-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



