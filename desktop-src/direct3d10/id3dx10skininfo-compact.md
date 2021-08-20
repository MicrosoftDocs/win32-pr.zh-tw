---
description: 限制可能影響頂點的骨骼數目，以及/或限制骨骼在頂點上可以有的影響數量。
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'ID3DX10SkinInfo：： Compact 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3aab3534ea55d2f6675ef1e65b03d19f4c516562b242e284ee2865f98bc03f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046906"
---
# <a name="id3dx10skininfocompact-method"></a>ID3DX10SkinInfo：： Compact 方法

限制可能影響頂點的骨骼數目，以及/或限制骨骼在頂點上可以有的影響數量。

## <a name="syntax"></a>語法


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MaxPerVertexInfluences* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

可以影響任何指定頂點的最大骨骼數目。 如果這個值大於 [**ID3DX10SkinInfo：： GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)所傳回的值，則會予以忽略。

</dd> <dt>

*ScaleMode* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

旗標，描述如何在某個頂點上的部分已由 MinWeight 切碎之後調整指定頂點上的剩餘權數。 如果未 \_ 指定 D3DX10 SKININFO \_ ，就 \_ 不會調整加權。 如果 \_ \_ 指定了 D3DX10 SKININFO SCALE \_ TO \_ 1，則權數大於 MinWeight 將會相應增加，使其增加到1.0。 如果 \_ \_ 指定了 D3DX10 SKININFO SCALE \_ TO \_ TOTAL，則權數大於 MinWeight 將會相應增加，使其增加至原始總計。

</dd> <dt>

*MinWeight* \[在\]
</dt> <dd>

類型： **float**

任何骨骼在任何頂點上可以有的影響（或權數）的最小百分比。 此值必須介於0和1之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是： E \_ OUTOFMEMORY 或 e \_ INVALIDARG。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
