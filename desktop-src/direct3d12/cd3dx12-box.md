---
title: 'CD3DX12_BOX 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ BOX 結構。
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX 結構
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982196"
---
# <a name="cd3dx12_box-structure"></a>CD3DX12 \_ BOX 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ BOX ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 BOX 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ box (CONST D3D12 \_ box& o)**
</dt> <dd>

建立 CD3DX12 方塊的新實例 \_ ，並使用另一個 [**D3D12 \_ 框**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) 結構的內容進行初始化。

</dd> <dt>

**明確的 CD3DX12 方塊 \_ (Long Left、Long Right)**
</dt> <dd>

建立 CD3DX12 BOX 的新實例 \_ ，並初始化下列參數：

長左方

長右邊

</dd> <dt>

**明確的 CD3DX12 方塊 \_ (Long 左方、Long Top、Long Right、Long 下)**
</dt> <dd>

建立 CD3DX12 BOX 的新實例 \_ ，並初始化下列參數：

長左方

長頂端

長右邊

長底部

</dd> <dt>

**明確的 CD3DX12 方塊 \_ (Long 左方、Long Top、Long Front、Right、LONG long、Long 後)**
</dt> <dd>

建立 CD3DX12 BOX 的新實例 \_ ，並初始化下列參數：

長左方

長頂端

長 Front

長右邊

長底部

長回來

</dd> <dt>

**~ CD3DX12 \_ BOX ()**
</dt> <dd>

終結 CD3DX12 BOX 的實例 \_ 。

</dd> <dt>

**運算子 const D3D12 \_ BOX& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





