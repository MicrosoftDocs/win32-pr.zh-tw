---
description: 取得技術描述。
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'ID3DXBaseEffect：： GetTechniqueDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196437"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a>ID3DXBaseEffect：： GetTechniqueDesc 方法

取得技術描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTechnique* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

技術控點。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pDesc* \[擴展\]
</dt> <dd>

類型： **[ **D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)\***

傳回技術的描述。 請參閱 [**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




