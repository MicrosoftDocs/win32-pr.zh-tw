---
description: 變更哪些頂點受哪些骨骼影響。
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo：： RemapVertices 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d73b9878a43ef876174561f16678f78787b15b88f423ecfb3f1765bd82c84630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302474"
---
# <a name="id3dx10skininforemapvertices-method"></a>ID3DX10SkinInfo：： RemapVertices 方法

變更哪些頂點受哪些骨骼影響。

## <a name="syntax"></a>語法


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewVertexCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

新的頂點數目。

</dd> <dt>

*pVertexRemap* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

指向頂點索引陣列的指標，其描述重新對應。 例如，假設 SkinInfo 包含一些頂點，例如 bone0 對應至 v0、bone1 至 v1，以及 bone2 為 v2，而且指定了2，1，0的陣列為 pBoneRemap。 這會導致 bone0 對應至 v2、bone1 至 v1，並 bone2 至 v0。

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

 

 
