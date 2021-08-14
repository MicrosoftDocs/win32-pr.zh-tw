---
description: 起始每個環境圖臉部的繪圖。
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap：：臉部方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1190e033f9aa83b13f327fcb8a8b530be17132bfd330c9be6b9cc6d87d5e35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801217"
---
# <a name="id3dxrendertoenvmapface-method"></a>ID3DXRenderToEnvMap：：臉部方法

起始每個環境圖臉部的繪圖。

## <a name="syntax"></a>語法


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*臉部* \[在\]
</dt> <dd>

類型： **[ **D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md)**

環境 cube 對應的第一個臉部。 請參閱 [**D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md)。

</dd> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選](d3dx-filter.md) 旗標的有效組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

您必須針對每個環境對應類型呼叫這個方法一次。 唯一的例外狀況是三次的環境對應，需要呼叫此方法六次，D3DCUBEMAP 臉部中的每個臉部 \_ 。 如需詳細資訊，請參閱 [ (Direct3D 9) 的環境對應 ](environment-mapping.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
