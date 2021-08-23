---
description: 提供取得和設定效果參數的方法，例如常數、函數、著色器和技術。
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: 'ID3DXBaseEffect 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8525a8139cd769a59886576f8ec32c7dab333a2903ffdb0fba1abc8ffbe27d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848548"
---
# <a name="id3dxbaseeffect-interface"></a>ID3DXBaseEffect 介面

提供取得和設定效果參數的方法，例如常數、函數、著色器和技術。

## <a name="members"></a>成員

**ID3DXBaseEffect** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXBaseEffect** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXBaseEffect** 介面具有這些方法。



| 方法                                                                                    | 描述                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnnotation**](id3dxbaseeffect--getannotation.md)                                   | 取得注釋的控制碼。 <br/>                                                                                                                                                                                     |
| [**GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md)                       | 藉由查詢名稱來取得批註的控制碼。<br/>                                                                                                                                                               |
| [**GetBool**](id3dxbaseeffect--getbool.md)                                               | 取得 BOOL 值。<br/>                                                                                                                                                                                                     |
| [**GetBoolArray**](id3dxbaseeffect--getboolarray.md)                                     | 取得 BOOL 值的陣列。<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | 取得效果描述。<br/>                                                                                                                                                                                           |
| [**GetFloat**](id3dxbaseeffect--getfloat.md)                                             | 取得浮點值。<br/>                                                                                                                                                                                           |
| [**GetFloatArray**](id3dxbaseeffect--getfloatarray.md)                                   | 取得浮點值的陣列。<br/>                                                                                                                                                                                |
| [**GetFunction**](id3dxbaseeffect--getfunction.md)                                       | 取得函數的控制碼。<br/>                                                                                                                                                                                         |
| [**GetFunctionByName**](id3dxbaseeffect--getfunctionbyname.md)                           | 藉由查詢名稱來取得函數的控制碼。<br/>                                                                                                                                                                  |
| [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)                               | 取得函數描述。<br/>                                                                                                                                                                                           |
| [**GetInt**](id3dxbaseeffect--getint.md)                                                 | 取得整數。<br/>                                                                                                                                                                                                       |
| [**GetIntArray**](id3dxbaseeffect--getintarray.md)                                       | 取得整數的陣列。<br/>                                                                                                                                                                                             |
| [**GetMatrix**](id3dxbaseeffect--getmatrix.md)                                           | 取得 nontransposed 矩陣。<br/>                                                                                                                                                                                           |
| [**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)                                 | 取得 nontransposed 矩陣的陣列。<br/>                                                                                                                                                                               |
| [**GetMatrixPointerArray**](id3dxbaseeffect--getmatrixpointerarray.md)                   | 取得 nontransposed 矩陣的指標陣列。<br/>                                                                                                                                                                   |
| [**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)                         | 取得已轉置的矩陣。<br/>                                                                                                                                                                                              |
| [**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)               | 取得已轉置矩陣的陣列。<br/>                                                                                                                                                                                  |
| [**GetMatrixTransposePointerArray**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | 取得已轉置矩陣的指標陣列。<br/>                                                                                                                                                                      |
| [**GetParameter**](id3dxbaseeffect--getparameter.md)                                     | 取得最上層參數或結構成員參數的控制碼。<br/>                                                                                                                                              |
| [**GetParameterByName**](id3dxbaseeffect--getparameterbyname.md)                         | 藉由查詢名稱來取得最上層參數或結構成員參數的控制碼。<br/>                                                                                                                       |
| [**GetParameterBySemantic**](id3dxbaseeffect--getparameterbysemantic.md)                 | 藉由使用不區分大小寫的搜尋來查閱其語義，取得最上層參數或結構成員參數的控制碼。<br/>                                                                                    |
| [**GetParameterDesc**](id3dxbaseeffect--getparameterdesc.md)                             | 取得參數或注釋描述。<br/>                                                                                                                                                                            |
| [**GetParameterElement**](id3dxbaseeffect--getparameterelement.md)                       | 取得陣列元素參數的控制碼。<br/>                                                                                                                                                                          |
| [**GetPass**](id3dxbaseeffect--getpass.md)                                               | 取得傳遞的控制碼。<br/>                                                                                                                                                                                             |
| [**GetPassByName**](id3dxbaseeffect--getpassbyname.md)                                   | 藉由查詢名稱來取得傳遞的控制碼。<br/>                                                                                                                                                                      |
| [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)                                       | 取得傳遞描述。<br/>                                                                                                                                                                                               |
| [**GetPixelShader**](id3dxbaseeffect--getpixelshader.md)                                 | 取得圖元著色器。<br/>                                                                                                                                                                                                   |
| [**GetString**](id3dxbaseeffect--getstring.md)                                           | 取得字串。<br/>                                                                                                                                                                                                         |
| [**GetTechnique**](id3dxbaseeffect--gettechnique.md)                                     | 取得技術的控制碼。<br/>                                                                                                                                                                                        |
| [**GetTechniqueByName**](id3dxbaseeffect--gettechniquebyname.md)                         | 藉由查詢名稱來取得技術的控制碼。<br/>                                                                                                                                                                 |
| [**GetTechniqueDesc**](id3dxbaseeffect--gettechniquedesc.md)                             | 取得技術描述。<br/>                                                                                                                                                                                          |
| [**GetTexture**](id3dxbaseeffect--gettexture.md)                                         | 取得材質。<br/>                                                                                                                                                                                                        |
| [**GetValue**](id3dxbaseeffect--getvalue.md)                                             | 取得任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。 這個方法可以用來取代 **ID3DXBaseEffect** 中幾乎所有的 Getxxx 呼叫。<br/> |
| [**GetVector**](id3dxbaseeffect--getvector.md)                                           | 取得向量。<br/>                                                                                                                                                                                                         |
| [**GetVectorArray**](id3dxbaseeffect--getvectorarray.md)                                 | 取得向量的陣列。<br/>                                                                                                                                                                                              |
| [**GetVertexShader**](id3dxbaseeffect--getvertexshader.md)                               | 取得頂點著色器。<br/>                                                                                                                                                                                                  |
| [**SetArrayRange**](id3dxbaseeffect--setarrayrange.md)                                   | 設定要傳遞至裝置的陣列範圍。<br/>                                                                                                                                                                       |
| [**SetBool**](id3dxbaseeffect--setbool.md)                                               | 設定布林值。<br/>                                                                                                                                                                                                     |
| [**SetBoolArray**](id3dxbaseeffect--setboolarray.md)                                     | 設定布林值的陣列。<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | 設定浮點值。<br/>                                                                                                                                                                                           |
| [**SetFloatArray**](id3dxbaseeffect--setfloatarray.md)                                   | 設定浮點值的陣列。<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | 設定整數。<br/>                                                                                                                                                                                                       |
| [**SetIntArray**](id3dxbaseeffect--setintarray.md)                                       | 設定整數的陣列。<br/>                                                                                                                                                                                             |
| [**SetMatrix**](id3dxbaseeffect--setmatrix.md)                                           | 設定非轉換的矩陣。<br/>                                                                                                                                                                                          |
| [**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)                                 | 設定 nontransposed 矩陣的陣列。<br/>                                                                                                                                                                               |
| [**SetMatrixPointerArray**](id3dxbaseeffect--setmatrixpointerarray.md)                   | 設定 nontransposed 矩陣的指標陣列。<br/>                                                                                                                                                                   |
| [**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)                         | 設定已轉置的矩陣。<br/>                                                                                                                                                                                              |
| [**SetMatrixTransposeArray**](id3dxbaseeffect--setmatrixtransposearray.md)               | 設定已轉置矩陣的陣列。<br/>                                                                                                                                                                                  |
| [**SetMatrixTransposePointerArray**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | 將指標的陣列設定為已轉置的矩陣。<br/>                                                                                                                                                                      |
| [**SetString**](id3dxbaseeffect--setstring.md)                                           | 設定字串。<br/>                                                                                                                                                                                                         |
| [**SetTexture**](id3dxbaseeffect--settexture.md)                                         | 設定紋理。<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | 設定任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。 <br/>                                                                                        |
| [**SetVector**](id3dxbaseeffect--setvector.md)                                           | 設定向量。<br/>                                                                                                                                                                                                         |
| [**SetVectorArray**](id3dxbaseeffect--setvectorarray.md)                                 | 設定向量的陣列。<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>備註

LPD3DXBASEEFFECT 型別定義為這個介面的指標。


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果介面](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
