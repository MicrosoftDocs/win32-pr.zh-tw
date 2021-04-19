---
description: 取得效果狀態管理員。
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect：： GetStateManager 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993866"
---
# <a name="id3dxeffectgetstatemanager-method"></a>ID3DXEffect：： GetStateManager 方法

取得效果狀態管理員。

## <a name="syntax"></a>語法


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppManager* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

傳回狀態管理員的指標。 請參閱 [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md)是使用者執行的介面，可將回呼提供至應用程式，以從效果設定裝置狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




