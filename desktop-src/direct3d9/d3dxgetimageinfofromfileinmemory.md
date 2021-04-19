---
description: 抓取記憶體中指定影像檔案的相關資訊。
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: 'D3DXGetImageInfoFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000591"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a>D3DXGetImageInfoFromFileInMemory 函式

抓取記憶體中指定影像檔案的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

記憶體中來源檔案的 VOID 指標。

</dd> <dt>

*SrcDataSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

記憶體中的檔案大小（以位元組為單位）。 .

</dd> <dt>

*pSrcInfo* \[在\]
</dt> <dd>

類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***

[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入原始程式檔中的資料描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFile**](d3dxgetimageinfofromfile.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
