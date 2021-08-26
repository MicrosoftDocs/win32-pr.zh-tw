---
description: D3DXGetImageInfoFromFile 函式-取得指定影像檔案的相關資訊。
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: 'D3DXGetImageInfoFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1726fae1697a48d8e4aa406f5eb5cec03f6071fed4b36a199b10e385a24e6249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027628"
---
# <a name="d3dxgetimageinfofromfile-function"></a>D3DXGetImageInfoFromFile 函式

抓取指定影像檔案的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcFile* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要取得相關資訊之影像的檔案名。 如果 \_ 已定義 unicode 或 unicode，則此參數類型為 LPCWSTR，否則為 LPCSTR 類型。

</dd> <dt>

*pSrcInfo* \[在\]
</dt> <dd>

類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***

[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入原始程式檔中的資料描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

此函數支援 Unicode 和 ANSI 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
