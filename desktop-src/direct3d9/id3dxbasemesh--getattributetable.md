---
description: ID3DXBaseMesh：： GetAttributeTable 方法-抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'ID3DXBaseMesh：： GetAttributeTable 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4933c3e15faee28448a653c5479be0d976abfd7bd913a7b50ef34acf4b52f6f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026498"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>ID3DXBaseMesh：： GetAttributeTable 方法

抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。

## <a name="syntax"></a>語法


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAttribTable* \[in、out\]
</dt> <dd>

類型： **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)結構陣列的指標，代表網格屬性工作表中的專案。 指定 **Null** 可取出 pAttribTableSize 的值。

</dd> <dt>

*pAttribTableSize* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

儲存在 pAttribTable 中的專案數或要填入的值的指標，該專案是以網格的屬性工作表中儲存的專案數來填滿。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

屬性資料表是由 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 和傳遞 D3DXMESHOPT ATTRSORT 的 \_ 旗標參數所建立。

屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。 此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時繪製指定的屬性識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
