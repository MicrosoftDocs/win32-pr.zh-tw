---
description: 從常數的陣列取得常數。 陣列是由元素所組成。
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable：： GetConstantElement 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb1adacadb92cf3a2f9a3e041e4a94a840994db3244233509350448008bd675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748778"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>ID3DXConstantTable：： GetConstantElement 方法

從常數的陣列取得常數。 陣列是由元素所組成。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hConstant* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

常數陣列的唯一識別碼。 此值不可以是 **Null**。

</dd> <dt>

*索引* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中元素之以零為起始的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回元素常數的唯一識別碼。

## <a name="remarks"></a>備註

若要取得不屬於陣列的常數，請使用 [**ID3DXConstantTable：： GetConstant**](id3dxconstanttable--getconstant.md) 或 [**ID3DXConstantTable：： GetConstantByName**](id3dxconstanttable--getconstantbyname.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
