---
title: 'CD3DX12_RT_FORMAT_ARRAY 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ RT \_ 格式 \_ 陣列結構。
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- CD3DX12_RT_FORMAT_ARRAY 結構
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9c153b98e84176d2682f028657176902fb68ebc0e8e1e52c69c196842dc2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988358"
---
# <a name="cd3dx12_rt_format_array-structure"></a>CD3DX12 \_ RT \_ 格式 \_ 陣列結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ RT \_ 格式 \_ 陣列 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ RT \_ 格式陣列實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ rt \_ 格式 \_ 陣列 (const D3D12 \_ RT \_ 格式 \_ 陣列& o)**
</dt> <dd>

建立 CD3DX12 \_ RT 格式陣列的新實例 \_ \_ ，並以從 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構複製而來的值進行初始化。

</dd> <dt>

**明確 \_ 的 CD3DX12 RT \_ 格式 \_ 陣列 (const DXGI \_ Format \* pFormats，UINT NumFormats)**
</dt> <dd>

建立 CD3DX12 \_ RT 格式陣列的新實例 \_ \_ ，並以參數清單中傳遞的值進行初始化。 *PFormats* 參數所指定的陣列內容會複製到成員陣列 **RTFormats** 中。 *PFormats* 指定的陣列會假設其大小與 **RTFormats** 相同。

</dd> <dt>

**operator const D3D12 \_ RT \_ 格式 \_ 陣列& () const**
</dt> <dd>

隱含轉換成 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。 因為 D3D12 \_ RT \_ 格式 \_ 陣列是 CD3DX12 深度樣板 DESC1 的基礎類型 \_ \_ \_ ，所以物件只會以 const D3D12 \_ RT \_ 格式陣列參考的形式傳回 \_ 本身。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





