---
title: 'CD3DX12_RANGE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 範圍結構。
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- CD3DX12_RANGE 結構
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999307"
---
# <a name="cd3dx12_range-structure"></a>CD3DX12 \_ 範圍結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 範圍 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 範圍實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 範圍 (CONST D3D12 \_ 範圍 &o)**
</dt> <dd>

建立 CD3DX12 範圍的新實例 \_ ，並使用另一個 [**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 範圍 (大小 \_ t 開頭，大小 \_ t 結束)**
</dt> <dd>

建立 CD3DX12 範圍的新實例 \_ ，並初始化下列參數：

大小 \_ T 開始

大小 \_ T 結束

</dd> <dt>

**運算子 const D3D12 \_ 範圍& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





