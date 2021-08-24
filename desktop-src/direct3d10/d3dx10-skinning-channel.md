---
description: 要在其上進行軟體外觀的頂點 decl 成員。 這可搭配 ID3DX10SkinInfo：:D oSoftwareSkinning API 使用。
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: 'D3DX10_SKINNING_CHANNEL 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b8e976ba1aecdeb792ba45fc4f60f25e7feb5a7dde3f7fc845a22962e441bf2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753528"
---
# <a name="d3dx10_skinning_channel-structure"></a>D3DX10 \_ 外觀 \_ 通道結構

要在其上進行軟體外觀的頂點 decl 成員。 這可搭配 [**ID3DX10SkinInfo：:D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) API 使用。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>成員

<dl> <dt>

**SrcOffset**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

從每個來源頂點的開頭算起的位移。

</dd> <dt>

**DestOffset**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

從每個目的地頂點的開頭算起的位移。

</dd> <dt>

**IsNormal**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

判斷要在 [**ID3DX10SkinInfo：:D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) API 中使用的矩陣陣列。 若為 true，則會使用 *pInverseTransposeBoneMatrices* ，否則會使用 *pBoneMatrices* 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
