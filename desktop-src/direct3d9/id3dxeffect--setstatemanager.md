---
description: 設定效果狀態管理員。
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'ID3DXEffect：： SetStateManager 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 06b6a7404f664e8ec18247b2eda57c5097cd575a3556853bfe8a9eb67705d071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295901"
---
# <a name="id3dxeffectsetstatemanager-method"></a>ID3DXEffect：： SetStateManager 方法

設定效果狀態管理員。

## <a name="syntax"></a>語法


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pManager* \[在\]
</dt> <dd>

類型： **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**

狀態管理員的指標。 請參閱 [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md)。

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

[**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




