---
description: 在頂點的陣列上進行軟體外觀。
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: 'ID3DX10SkinInfo：:D oSoftwareSkinning 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f68f51d6886d53d74cd31691e52c362c60d2bf9be2beb0656564cb20fcb80a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729808"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo：:D oSoftwareSkinning 方法

在頂點的陣列上進行軟體外觀。

## <a name="syntax"></a>語法


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartVertex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PSrcVertices 的以零為基的索引。

</dd> <dt>

*VertexCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要轉換的頂點數目。

</dd> <dt>

*pSrcVertices* \[在\]
</dt> <dd>

類型： **void \***

要轉換之頂點陣列的指標。

</dd> <dt>

*SrcStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PSrcVertices 中頂點的大小（以位元組為單位）。

</dd> <dt>

*pDestVertices* \[in、out\]
</dt> <dd>

類型： **void \***

指向頂點陣列的指標，將會填入已轉換的頂點。

</dd> <dt>

*DestStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PDestVertices 中頂點的大小（以位元組為單位）。

</dd> <dt>

*pBoneMatrices* \[在\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

矩陣的陣列，將用來轉換對應至每個骨骼的點，以便 \[ \] pBoneMatrices i 轉換對應至骨骼的頂點 \[ \] 。 只有在 pChannelDescs 中的 IsNormal 值設定為 **FALSE** 時，才會使用這個陣列來轉換矩陣，否則會使用 pInverseTransposeBoneMatrices。

</dd> <dt>

*pInverseTransposeBoneMatrices* \[在\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

如果這個值為 **Null**，則會設定為等於 pBoneMatrices。 只有在 pChannelDescs 中的 IsNormal 值設定為 **TRUE** 時，才會使用此矩陣陣列來轉換頂點，否則會使用 pBoneMatrices。

</dd> <dt>

*pChannelDescs* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 外觀 \_ 通道**](d3dx10-skinning-channel.md)\***

D3DX10 \_ 外觀 \_ 通道結構的指標，它會決定要對其執行軟體外觀的頂點 decl 成員。

</dd> <dt>

*NumChannels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PChannelDescs 中 D3DX10 的 \_ 外觀 \_ 通道結構數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是： E \_ INVALIDARG。

## <a name="remarks"></a>備註

以下是如何使用軟體外觀的範例：


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



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

 

 
