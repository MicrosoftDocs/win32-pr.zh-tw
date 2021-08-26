---
description: ID3DXTextureShader 介面。
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: 'ID3DXTextureShader 介面 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95e6a8feb35ea5d1e38a5cb63bb1379e4995e7562839cc1b582ee8efd8550212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846978"
---
# <a name="id3dxtextureshader-interface"></a>ID3DXTextureShader 介面

ID3DXTextureShader 介面。

## <a name="members"></a>成員

**ID3DXTextureShader** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXTextureShader** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXTextureShader** 介面具有這些方法。



| 方法                                                                                       | 描述                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**GetConstant**](id3dxtextureshader--getconstant.md)                                       | 藉由查閱索引來取得常數。<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | 取得常數資料表的指標。<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | 藉由查詢名稱來取得常數。<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | 取得常數資料表中常數陣列的指標。<br/>  |
| [**GetConstantElement**](id3dxtextureshader--getconstantelement.md)                         | 從常數資料表取得常數。<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | 取得常數資料表的描述。<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | 取得函數 DWORD 資料流程的指標。<br/>                     |
| [**SetBool**](id3dxtextureshader--setbool.md)                                               | 設定布林值。<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | 設定 BOOL 值的陣列。<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | 將常數設定為著色器中宣告的預設值。<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | 設定浮點數。<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | 設定浮點數字的陣列。<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | 設定整數值。<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | 設定整數的陣列。<br/>                                       |
| [**SetMatrix**](id3dxtextureshader--setmatrix.md)                                           | 設定非轉換的矩陣。<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | 設定非轉換矩陣的陣列。<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | 將指標的陣列設定為非轉換的矩陣。<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | 設定已轉置的矩陣。<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | 設定已轉置矩陣的陣列。<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | 將指標的陣列設定為已轉置的矩陣。<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | 使用緩衝區中的資料來設定常數資料表。<br/>             |
| [**SetVector**](id3dxtextureshader--setvector.md)                                           | 設定4D 向量。<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | 設定4D 向量的陣列。<br/>                                     |



 

## <a name="remarks"></a>備註

**ID3DXTextureShader** 介面是藉由呼叫 [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md)函數來取得。

**ID3DXTextureShader** 介面就像所有的 COM 介面，會繼承 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。

LPD3DXTEXTURESHADER 型別定義為 **ID3DXTextureShader** 介面的指標。


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
