---
title: 'D3D12_RECT (D3D12) '
description: D3D12 \_ rect 宣告為 rect。
ms.assetid: 39511ACE-7AC5-42A2-896D-7E0977A346C6
keywords:
- D3D12_RECT
topic_type:
- apiref
api_name:
- D3D12_RECT
api_location:
- D3D12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951c0de8468b0384ae1a474740f9b46c2aa68dfc23c3394f8dae6a8064d9319e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751728"
---
# <a name="d3d12_rect"></a>D3D12 \_ RECT

D3D12 \_ rect 宣告為 rect。 如需有關此 GDI 矩形結構的詳細資訊，請參閱 [**RECT**](/previous-versions//dd162897(v=vs.85))。

``` syntax
typedef RECT D3D12_RECT;
```

## <a name="remarks"></a>備註

下列方法會使用此結構：

-   [**RSSetScissorRects**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)

此結構是 [**D3D12 \_ 捨棄 \_ 區域**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) 結構的成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心結構](direct3d-12-structures.md)
</dt> <dt>

[**CD3DX12 \_ RECT**](cd3dx12-rect.md)
</dt> </dl>

 

