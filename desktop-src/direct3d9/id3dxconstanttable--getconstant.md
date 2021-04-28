---
description: ID3DXConstantTable：： GetConstant 方法-藉由查閱索引來取得常數。
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'ID3DXConstantTable：： GetConstant 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115266"
---
# <a name="id3dxconstanttablegetconstant-method"></a>ID3DXConstantTable：： GetConstant 方法

藉由查閱索引來取得常數。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hConstant* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

父資料結構的唯一識別碼。 如果常數是最上層參數 (沒有任何父資料結構) ，請使用 **Null**。

</dd> <dt>

*索引* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

常數以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回常數的唯一識別碼。

## <a name="remarks"></a>備註

若要從常數陣列取得常數，請使用 [**ID3DXConstantTable：： GetConstantElement**](id3dxconstanttable--getconstantelement.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
