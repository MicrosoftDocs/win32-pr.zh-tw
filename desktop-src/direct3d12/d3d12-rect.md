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
ms.openlocfilehash: d408832e800413f94e251ee27a57e5b326378c36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997238"
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

 

