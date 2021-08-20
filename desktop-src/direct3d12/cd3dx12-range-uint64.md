---
title: 'CD3DX12_RANGE_UINT64 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 範圍 \_ UINT64 結構。
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- CD3DX12_RANGE_UINT64 結構
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a07cb6a095c707b06b5b9982d29d73bb7bb9b6a32fca02233c50298a9804065a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098697"
---
# <a name="cd3dx12_range_uint64-structure"></a>CD3DX12 \_ 範圍 \_ UINT64 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 範圍 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 範圍 \_ UINT64 ()**
</dt> <dd>

建立 CD3DX12 範圍 UINT64 的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 範圍 \_ uint64 (const D3D12 \_ range \_ uint64 &o)**
</dt> <dd>

建立 CD3DX12 範圍 uint64 的新實例 \_ \_ ，並以從 [**D3D12 \_ 範圍 \_ uint64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) 結構複製而來的值進行初始化。

</dd> <dt>

**CD3DX12 \_ 範圍 \_ UINT64 (uint64 BEGIN，uint64 end)**
</dt> <dd>

建立 CD3DX12 深度樣板 DESC1 的新 \_ 實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。

</dd> <dt>

**運算子 const D3D12 \_ RANGE \_ UINT64& () const**
</dt> <dd>

隱含轉換成 D3D12 \_ 範圍 \_ UINT64 結構。 因為 D3D12 \_ 範圍 \_ UINT64 是 CD3DX12 範圍 uint64 的基礎 \_ 類型 \_ ，所以物件會直接傳回為 const D3D12 \_ RANGE \_ uint64 參考本身。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ 範圍 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





