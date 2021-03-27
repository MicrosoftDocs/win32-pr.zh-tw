---
title: 'D3D11_RECT (D3D11) '
description: D3D11 \_ RECT 的宣告方式如下
ms.assetid: d1cbbbd7-1221-4706-b805-8422c5ebdadc
keywords:
- D3D11_RECT Direct3D 11
topic_type:
- apiref
api_name:
- D3D11_RECT
api_location:
- D3D11.lib
- D3D11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7fac5627c74123c977aac379826d5264d767ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854068"
---
# <a name="d3d11_rect"></a>D3D11 \_ RECT

D3D11 \_ RECT 的宣告方式如下：

``` syntax
typedef RECT D3D11_RECT;
```

如需有關此 GDI 矩形結構的詳細資訊，請參閱 [**RECT**](/previous-versions//dd162897(v=vs.85))。

## <a name="remarks"></a>備註

[**>id3d11devicecoNtext：： RSGetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rsgetscissorrects)和 [**>id3d11devicecoNtext：： RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects)的剪式矩形會使用此結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3D11。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3D11 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心結構](d3d11-graphics-reference-d3d11-core-structures.md)
</dt> </dl>

 

