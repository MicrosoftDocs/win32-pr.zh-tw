---
description: ID3DXTextureShader：： GetDesc 方法-取得常數資料表的描述。
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'ID3DXTextureShader：： GetDesc 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06619730ceaa03dfdc812c669726bcde032caf7380ce4a7736085ee3a62b9d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729021"
---
# <a name="id3dxtextureshadergetdesc-method"></a>ID3DXTextureShader：： GetDesc 方法

取得常數資料表的描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* \[在\]
</dt> <dd>

類型： **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***

常數資料表的屬性。 請參閱 [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




