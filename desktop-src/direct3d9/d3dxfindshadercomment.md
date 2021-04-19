---
description: 在著色器中搜尋特定批註。 批註會以四個字元的程式碼識別， (FOURCC) 在批註的第一個 DWORD 中。
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: 'D3DXFindShaderComment 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982879"
---
# <a name="d3dxfindshadercomment-function"></a>D3DXFindShaderComment 函式

在著色器中搜尋特定批註。 批註會以四個字元的程式碼識別， (FOURCC) 在批註的第一個 DWORD 中。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

著色器函式 DWORD 資料流程的指標。

</dd> <dt>

*FourCC* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

FOURCC 識別批註區塊的程式碼。 請參閱 [FourCC 格式](d3dformat.md)。

</dd> <dt>

*ppData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)\***

傳回批註資料的指標， (不包含註解標記和 FOURCC 程式碼) 。 這個值可以是 **Null**。

</dd> <dt>

*pSizeInBytes* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

傳回批註資料的大小（以位元組為單位）。 這個值可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果找不到批註，且未發生其他錯誤， \_ 則會傳回 FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
