---
title: XMINT4 結構
description: 描述4D 的整數向量。
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4 結構 HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323128"
---
# <a name="xmint4-structure"></a>XMINT4 結構

描述4D 的整數向量。

## <a name="syntax"></a>語法


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a>成員

<dl> <dt>

**x**
</dt> <dd>

向量的 x 元件。

</dd> <dt>

**y**
</dt> <dd>

向量的 y 元件。

<dl> <dt>

**Z**
</dt> <dd>

向量的 z 元件。

<dl> <dt>

**w**
</dt> <dd>

w-向量的元件。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. .inl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[結構](format-conversion-structures.md)
</dt> <dt>

[\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





