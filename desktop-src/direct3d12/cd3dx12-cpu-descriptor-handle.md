---
title: 'CD3DX12_CPU_DESCRIPTOR_HANDLE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ CPU \_ 描述項 \_ 控制碼結構。
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- CD3DX12_CPU_DESCRIPTOR_HANDLE 結構
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e6fd6ba75caccf19f3782e0c39581d1e652de0c4187c3c5a203bb5f3b7ceec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913075"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>CD3DX12 \_ CPU \_ 描述項 \_ 控制碼結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ CPU 描述項 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ CPU \_ 描述項 \_ 控制碼 ()**
</dt> <dd>

建立 CD3DX12 \_ CPU \_ 描述項控制碼的新、未初始化的實例 \_ 。

</dd> <dt>

**明確 CD3DX12 的 \_ cpu \_ 描述項 \_ 控制碼 (const D3D12 \_ cpu 描述項 \_ \_ 控制碼 &o)**
</dt> <dd>

建立 CD3DX12 \_ CPU 描述元控制碼的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ cpu 描述元 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ CPU \_ 描述項 \_ 控制碼 (CD3DX12 \_ 預設)**
</dt> <dd>

建立 CD3DX12 \_ CPU 描述元控制碼的新實例 \_ \_ ，並使用預設參數初始化 (指標設定為零) 。

</dd> <dt>

**CD3DX12 \_ cpu \_ 描述項 \_ 控制碼 (const D3D12 \_ cpu \_ 描述項 \_ 控制碼，&其他，INT offsetScaledByIncrementSize)**
</dt> <dd>

建立 CD3DX12 \_ CPU 描述項控制碼的新實例 \_ ，並 \_ 初始化下列參數：

D3D12 \_ CPU \_ 描述項 \_ 控制碼 &其他

INT offsetScaledByIncrementSize：位移的遞增數目。

</dd> <dt>

**CD3DX12 \_ cpu \_ 描述項 \_ 控制碼 (const D3D12 \_ cpu \_ 描述項 \_ 控制碼，&其他，INT offsetInDescriptors，UINT descriptorIncrementSize)**
</dt> <dd>

建立 CD3DX12 \_ CPU 描述項控制碼的新實例 \_ ，並 \_ 初始化下列參數：

D3D12 \_ CPU \_ 描述項 \_ 控制碼 &其他

INT offsetInDescriptors：要遞增的描述項數目。

UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。

</dd> <dt>

**Offset (INT offsetInDescriptors，UINT descriptorIncrementSize)**
</dt> <dd>

根據指定的描述項數目和每個描述項的遞增量，設定位移。 使用下列參數：

INT offsetInDescriptors：要遞增的描述項數目。

UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。

</dd> <dt>

**Offset (INT offsetScaledByIncrementSize)**
</dt> <dd>

根據指定的增量數目來設定位移。 使用下列參數：

INT offsetScaledByIncrementSize：位移的遞增數目。

</dd> <dt>

**operator = = ( \_ 在 \_ const D3D12 \_ 中 \_ \_& 其他) const 的 CPU 描述項控制碼**
</dt> <dd>

測試目前 CD3DX12 的 \_ cpu \_ 描述項 \_ 控制碼和指定的 D3D12 cpu 描述項控制碼是否相等， \_ \_ \_ 或 CD3DX12 \_ cpu 描述項 \_ \_ 控制碼。

</dd> <dt>

**operator！ = (\_ \_ const D3D12 \_ CPU 描述 \_ 項 \_ 控制碼& 其他) const**
</dt> <dd>

測試目前 CD3DX12 \_ cpu \_ 描述項 \_ 控制碼和指定的 D3D12 cpu 描述項控制碼之間是否不相等， \_ \_ \_ 或 CD3DX12 的 \_ cpu \_ 描述項 \_ 控制碼。

</dd> <dt>

**operator = (const D3D12 \_ CPU \_ 描述項 \_ 控制碼 &其他)**
</dt> <dd>

將目前的 CD3DX12 \_ cpu \_ 描述項 \_ 控制碼設定為與指定的 D3D12 \_ cpu \_ 描述項 \_ 控制碼或 CD3DX12 \_ cpu 描述項 \_ \_ 控制碼相同的值。

</dd> <dt>

**內嵌 InitOffsetted (\_ In \_ const D3D12 \_ CPU \_ 描述項 \_ 控制碼 &base，INT offsetScaledByIncrementSize)**
</dt> <dd>

使用指定的專案數，初始化 [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構。 使用下列參數：

\_在 \_ CONST D3D12 \_ 中 \_ ，CPU 描述項 \_ 控制碼 &基底：要從中位移的基底位址。

INT offsetScaledByIncrementSize：位移的遞增數目。

</dd> <dt>

**內嵌 InitOffsetted (\_ \_ const D3D12 \_ CPU 描述 \_ 項 \_ 控制碼 &BASE，INT offsetInDescriptors，UINT descriptorIncrementSize)**
</dt> <dd>

使用指定大小的指定數量描述元，初始化具有位移的 [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構。 使用下列參數：

\_在 \_ CONST D3D12 \_ 中 \_ ，CPU 描述項 \_ 控制碼 &基底：要從中位移的基底位址。

INT offsetInDescriptors：要位移的描述項數目。

UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。

</dd> <dt>

**靜態內嵌 InitOffsetted (\_ Out \_ D3D12 \_ cpu \_ 描述 \_ 項 &控制碼， \_ 在 \_ const D3D12 \_ CPU 描述項 \_ \_ 控制碼 &base，INT offsetScaledByIncrementSize)**
</dt> <dd>

使用指定大小的指定數量描述元，初始化具有位移的 [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構。 使用下列參數：

\_Out \_ D3D12 \_ cpu \_ 描述項 \_ 控制碼 &控制碼：輸出產生的 D3D12 \_ cpu \_ 描述項 \_ 控制碼。

\_在 \_ CONST D3D12 \_ 中 \_ ，CPU 描述項 \_ 控制碼 &基底：要從中位移的基底位址。

INT offsetScaledByIncrementSize：位移的遞增數目。

</dd> <dt>

**靜態內嵌 InitOffsetted (\_ Out \_ D3D12 \_ cpu \_ 描述 \_ 項 &控制碼， \_ 在 \_ const D3D12 \_ CPU 描述項 \_ \_ 控制碼 &base，INT offsetInDescriptors，UINT descriptorIncrementSize)**
</dt> <dd>

使用指定大小的指定數量描述元，初始化具有位移的 [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構。 使用下列參數：

\_Out \_ D3D12 \_ cpu \_ 描述項 \_ 控制碼 &控制碼：輸出產生的 D3D12 \_ cpu \_ 描述項 \_ 控制碼。

\_在 \_ CONST D3D12 \_ 中 \_ ，CPU 描述項 \_ 控制碼 &基底：要從中位移的基底位址。

INT offsetInDescriptors：要位移的描述項數目。

UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





