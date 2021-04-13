---
description: 還原所有呈現目標，並視需要將所有呈現的臉部組成環境地圖介面。
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'ID3DXRenderToEnvMap：： End 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322803"
---
# <a name="id3dxrendertoenvmapend-method"></a>ID3DXRenderToEnvMap：： End 方法

還原所有呈現目標，並視需要將所有呈現的臉部組成環境地圖介面。

## <a name="syntax"></a>語法


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選](d3dx-filter.md) 旗標的有效組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap：：臉部**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
