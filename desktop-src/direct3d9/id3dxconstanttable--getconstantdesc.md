---
description: 取得常數資料表中常數描述陣列的指標。
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable：： GetConstantDesc 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8462ccfbbf306da08c67d460584a470d82301a5bda5f95a1ad09b2062702ee62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607208"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>ID3DXConstantTable：： GetConstantDesc 方法

取得常數資料表中常數描述陣列的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hConstant* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

常數的唯一識別碼。 請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。

</dd> <dt>

*pDesc* \[in、out\]
</dt> <dd>

類型： **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

傳回描述陣列的指標。 請參閱 [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)。

</dd> <dt>

*pCount* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

提供的輸入必須是陣列的大小上限。 輸出是當函式傳回時，在陣列中填入的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

**ID3DXConstantTable：： GetConstantDesc** 有時會傳回註冊計數為0的 [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) \_ 。 發生這種情況時，常數會出現在一個以上的暫存器 \_ 集中，但不會在該暫存器集合中配置任何空間。

因為取樣器可能在常數資料表中出現一次以上，所以這個方法可以傳回描述的陣列，每一個都有不同的暫存器索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetDesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
