---
description: D3D10 \_ RECT 的宣告方式如下：
ms.assetid: a0b27fb0-1e48-4e46-ad8c-99f197c31dc2
title: 'D3D10_RECT (D3D10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235a991942d2c6feba6070c4da3bb281692cbd6e0de69dc3cdfb9214ef60fb2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634998"
---
# <a name="d3d10_rect"></a>D3D10 \_ RECT

D3D10 \_ RECT 的宣告方式如下：

``` syntax
typedef RECT D3D10_RECT;
```

如需有關此 GDI 矩形結構的詳細資訊，請參閱 [RECT](/previous-versions//ms536136(v=vs.85))。

## <a name="remarks"></a>備註

[**ID3D10Device：： RSGetScissorRects**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rsgetscissorrects)和 [**ID3D10Device：： RSSetScissorRects**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetscissorrects)的剪式矩形會使用此結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3D10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3D10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心結構](d3d10-graphics-reference-d3d10-core-structures.md)
</dt> </dl>

 

 
