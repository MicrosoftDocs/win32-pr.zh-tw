---
description: ID3DXConstantTable 介面是用來存取常數資料表。 此資料表包含高階語言著色器和效果所使用的變數。
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: 'ID3DXConstantTable 介面 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982210"
---
# <a name="id3dxconstanttable-interface"></a>ID3DXConstantTable 介面

ID3DXConstantTable 介面是用來存取常數資料表。 此資料表包含高階語言著色器和效果所使用的變數。

## <a name="members"></a>成員

**ID3DXConstantTable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXConstantTable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXConstantTable** 介面具有這些方法。



| 方法                                                                                       | 描述                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | 取得包含常數資料表之緩衝區的指標。<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | 取得常數資料表的緩衝區大小。<br/>                                                                             |
| [**GetConstant**](id3dxconstanttable--getconstant.md)                                       | 藉由查閱索引來取得常數。<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | 藉由查詢名稱來取得常數。<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | 取得常數資料表中常數描述陣列的指標。<br/>                                              |
| [**GetConstantElement**](id3dxconstanttable--getconstantelement.md)                         | 從常數的陣列取得常數。 陣列是由元素所組成。<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | 取得常數資料表的描述。<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | 傳回取樣器索引。<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | 設定布林值。<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | 設定布林值的陣列。<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | 將常數設定為其預設值。 預設值會在著色器的變數宣告中宣告。<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | 設定浮點數。<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | 設定浮點數字的陣列。<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | 設定整數值。<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | 設定整數的陣列。<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | 設定 nontransposed 矩陣。<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | 設定 nontransposed 矩陣的陣列。<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | 設定 nontransposed 矩陣的指標陣列。<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | 設定已轉置的矩陣。<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | 設定已轉置矩陣的陣列。<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | 將指標的陣列設定為已轉置的矩陣。<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | 將緩衝區的內容設定為常數資料表。<br/>                                                                  |
| [**SetVector**](id3dxconstanttable--setvector.md)                                           | 設定4D 向量。<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | 設定4D 向量的陣列。<br/>                                                                                            |



 

## <a name="remarks"></a>備註

LPD3DXCONSTANTTABLE 型別定義為 **ID3DXConstantTable** 介面的指標。


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
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

 

 
