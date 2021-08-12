---
description: ID3DX10Mesh：： GetAttributeTable 方法-抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh：： GetAttributeTable 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce1f2464882bfdece8997aeea23f2bb42c276b3f6ce49b13cb242d517a522250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540288"
---
# <a name="id3dx10meshgetattributetable-method"></a>ID3DX10Mesh：： GetAttributeTable 方法

抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。

## <a name="syntax"></a>語法


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAttribTable* \[在\]
</dt> <dd>

Type： **[ **D3DX10 \_ 屬性 \_ 範圍**](d3dx10-attribute-range.md)\***

D3DX10 \_ 屬性範圍結構的陣列指標 \_ ，表示網格屬性工作表中的專案。 指定 **Null** 可取出 pAttribTableSize 的值。

</dd> <dt>

*pAttribTableSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

儲存在 pAttribTable 中的專案數或要填入的值的指標，該專案是以網格的屬性工作表中儲存的專案數來填滿。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。 此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時繪製指定的屬性識別碼。

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

 

 
