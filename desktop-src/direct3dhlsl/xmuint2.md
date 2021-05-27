---
title: XMUINT2 結構
description: 描述2D 不帶正負號的整數向量。
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2 結構 HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549563"
---
# <a name="xmuint2-structure"></a>XMUINT2 結構

描述2D 不帶正負號的整數向量。

## <a name="syntax"></a>語法


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
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

</dd> </dl>



## <a name="remarks"></a>備註

此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。 在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) 。



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