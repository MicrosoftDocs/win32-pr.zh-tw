---
description: 使用宣告子建立空白的外觀網格物件。
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: 'D3DX10CreateSkinInfo 函式 (D3DX10Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a68da20c2e2e15e3b73d55ee1df70518bba46200
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986762"
---
# <a name="d3dx10createskininfo-function"></a>D3DX10CreateSkinInfo 函式

使用宣告子建立空白的外觀網格物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSkinInfo* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

[**ID3DX10SkinInfo 介面**](id3dx10skininfo.md)指標的位址，表示所建立的面板網格物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是： E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用 [**ID3DX10SkinInfo：： SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) 來填入這個方法所傳回的空白麵板網格物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX 函式](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




