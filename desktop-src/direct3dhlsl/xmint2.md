---
title: XMINT2 結構
description: 描述2D 整數向量。
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2 結構 HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222856"
---
# <a name="xmint2-structure"></a>XMINT2 結構

描述2D 整數向量。

## <a name="syntax"></a>語法


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
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

此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。 在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) 。



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
