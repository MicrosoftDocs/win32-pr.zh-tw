---
title: XMUINT4 結構
description: 描述4D 不帶正負號的整數向量。
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 結構 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932168d2d251d5506727503053cb56cab2e50e57209276649beb35932478ab26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981468"
---
# <a name="xmuint4-structure"></a>XMUINT4 結構

描述4D 不帶正負號的整數向量。

## <a name="syntax"></a>語法


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
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

**z**
</dt> <dd>

向量的 z 元件。

<dl> <dt>

**w**
</dt> <dd>

w-向量的元件。

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>備註

此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。 在[DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的[DirectX：： XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) 。




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