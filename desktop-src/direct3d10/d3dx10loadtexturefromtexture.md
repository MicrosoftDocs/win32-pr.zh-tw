---
description: 從材質載入紋理。
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: 'D3DX10LoadTextureFromTexture 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: bfc36423154bfd56f0695a3a8178b89aefce6e4dfc5a67f3866fa13a99c5e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990498"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>D3DX10LoadTextureFromTexture 函式

從材質載入紋理。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcTexture* 
</dt> <dd>

類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

來源紋理的指標。 請參閱 [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

類型： **[ **D3DX10 \_ 材質 \_ 載入 \_ 資訊**](d3dx10-texture-load-info.md)\***

材質載入參數的指標。 請參閱 [**D3DX10 \_ 材質 \_ 載入 \_ 資訊**](d3dx10-texture-load-info.md)。

</dd> <dt>

*pDstTexture* 
</dt> <dd>

類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

目的地材質的指標。 請參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 10 中的材質函數](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




