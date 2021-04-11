---
description: 設定網格的屬性工作表和儲存在資料表中的專案數目。
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'ID3DX10Mesh：： SetAttributeTable 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196353"
---
# <a name="id3dx10meshsetattributetable-method"></a>ID3DX10Mesh：： SetAttributeTable 方法

設定網格的屬性工作表和儲存在資料表中的專案數目。

## <a name="syntax"></a>語法


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAttribTable* \[在\]
</dt> <dd>

Type： **Const [**D3DX10 \_ 屬性 \_ 範圍**](d3dx10-attribute-range.md) \***

D3DX10 \_ 屬性範圍結構的陣列指標 \_ ，表示網格屬性工作表中的專案。

</dd> <dt>

*cAttribTableSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

網格屬性工作表中的屬性數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

如果應用程式會追蹤屬性工作表中的資訊，並重新排列資料表，使其成為屬性或臉部變更的結果，此方法可讓應用程式更新屬性工作表，而不是再次呼叫 ID3DX10Mesh：： Optimize。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
