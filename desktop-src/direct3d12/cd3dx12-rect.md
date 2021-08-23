---
title: 'CD3DX12_RECT 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ RECT 結構。
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT 結構
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff9df3a4c7df2f30e9614b16d5f8b89ea1b6f0279a1566b206cabef7260fb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729338"
---
# <a name="cd3dx12_rect-structure"></a>CD3DX12 \_ RECT 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ RECT**](d3d12-rect.md) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ RECT ()**
</dt> <dd>

建立 CD3DX12 RECT 的新、未初始化的實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ RECT (CONST D3D12 \_ rect& o)**
</dt> <dd>

建立 CD3DX12 RECT 的新實例 \_ ，並使用另一個 [**D3D12 \_ RECT**](d3d12-rect.md) 結構的內容進行初始化。

</dd> <dt>

**明確的 CD3DX12 \_ 矩形 (Long 左方、Long Top、Long Right、Long 下)**
</dt> <dd>

建立 CD3DX12 RECT 的新實例 \_ ，並初始化下列參數：

長左方

長頂端

長右邊

長底部

</dd> <dt>

**~ CD3DX12 \_ RECT ()**
</dt> <dd>

終結 CD3DX12 RECT 的實例 \_ 。

</dd> <dt>

**運算子 const D3D12 \_ RECT& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ RECT**](d3d12-rect.md)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





