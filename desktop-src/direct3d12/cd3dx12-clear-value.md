---
title: 'CD3DX12_CLEAR_VALUE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 的 \_ 清除 \_ 值結構。
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE 結構
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000571"
---
# <a name="cd3dx12_clear_value-structure"></a>CD3DX12 \_ 清除 \_ 值結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 的 \_ 清除 \_ 值**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ CLEAR \_ VALUE ()**
</dt> <dd>

建立 CD3DX12 清除值的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ clear \_ 值 (const D3D12 \_ clear \_ value &o)**
</dt> <dd>

建立 CD3DX12 清除值的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 清除 \_ 值**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE (DXGI \_ 格式格式，const FLOAT color \[ 4 \])**
</dt> <dd>

建立 CD3DX12 清除值的新實例 \_ \_ ，並初始化下列參數：

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

浮點數色彩 \[ 4 \]

</dd> <dt>

**CD3DX12 \_ CLEAR \_ 值 (DXGI \_ 格式格式、浮點數深度、UINT8 樣板)**
</dt> <dd>

建立 CD3DX12 清除值的新實例 \_ \_ ，並初始化下列參數：

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

浮點數深度

UINT8 樣板

</dd> <dt>

**運算子 const D3D12 \_ CLEAR \_ VALUE& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ CLEAR \_ 值**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

