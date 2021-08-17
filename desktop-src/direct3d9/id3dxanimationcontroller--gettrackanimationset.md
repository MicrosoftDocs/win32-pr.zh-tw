---
description: 取得指定之播放軌的動畫集。
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'ID3DXAnimationController：： GetTrackAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23ee81fa6e704e73c1bf1a8e3064a5832731f2e5336e9725d3666409133a5106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122109"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a>ID3DXAnimationController：： GetTrackAnimationSet 方法

取得指定之播放軌的動畫集。

## <a name="syntax"></a>語法


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

追蹤識別碼。

</dd> <dt>

*ppAnimSet* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

針對給定的播放軌所設定的 [**ID3DXAnimationSet**](id3dxanimationset.md) 動畫指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
