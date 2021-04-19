---
title: 'CD3DX12_VIEWPORT 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 的 \_ 視口結構。
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- CD3DX12_VIEWPORT 結構
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985911"
---
# <a name="cd3dx12_viewport-structure"></a>CD3DX12 的 \_ 視口結構

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

協助程式結構，可讓您輕鬆地初始化 [**D3D12 的 \_ 視口**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 視口 ()**
</dt> <dd>

建立 CD3DX12 區的新、未初始化的實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 區 (CONST D3D12 \_ 視口& o)**
</dt> <dd>

建立 CD3DX12 區的新實例 \_ ，並初始化下列參數：

const D3D12 \_ 視口& o

</dd> <dt>

**明確的 CD3DX12 \_ 區 (Float topLeftX、Float topLeftY、float width、float height、Float minDepth = D3D12 \_ MIN \_ Depth、FLOAT maxDepth = D3D12 \_ MAX \_ depth)**
</dt> <dd>

建立 CD3DX12 區的新實例 \_ ，並初始化下列參數：

FLOAT topLeftX

FLOAT topLeftY

浮點數寬度

浮點數高度

FLOAT minDepth = D3D12 \_ MIN \_ DEPTH

FLOAT maxDepth = D3D12 \_ 最大 \_ 深度

</dd> <dt>

**明確 \_ 的 CD3DX12 區 (ID3D12Resource \* PRESOURCE，UINT mipSlice = 0，FLOAT topLeftX = 0.0 f，float topLeftY = 0.0 f，FLOAT MINDEPTH = D3D12 \_ MIN \_ depth，float maxDepth = D3D12 \_ MAX \_ depth)**
</dt> <dd>

建立 CD3DX12 區的新實例 \_ ，並初始化下列參數：

ID3D12Resource \* pResource

UINT mipSlice = 0

FLOAT topLeftX = 0.0 f

FLOAT topLeftY = 0.0 f

FLOAT minDepth = D3D12 \_ MIN \_ DEPTH

FLOAT maxDepth = D3D12 \_ 最大 \_ 深度

</dd> <dt>

**~ CD3DX12 的 \_ 視口 ()**
</dt> <dd>

終結 D3DX12 區的實例 \_ 。

</dd> <dt>

**運算子 const D3D12 \_ 視口& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 區**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





