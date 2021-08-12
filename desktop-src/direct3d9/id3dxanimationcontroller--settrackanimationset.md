---
description: 將動畫集套用至指定的曲目。
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController：： SetTrackAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a94fee2a0bd80f391b514895aa5b5348cbef6d8a53e31200b49a403a6712e2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296881"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>ID3DXAnimationController：： SetTrackAnimationSet 方法

將動畫集套用至指定的曲目。

## <a name="syntax"></a>語法


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

套用動畫集之追蹤的識別碼。

</dd> <dt>

*pAnimSet* \[在\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

要加入至曲目的 [**ID3DXAnimationSet**](id3dxanimationset.md) 動畫指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會將動畫設定為混合的指定追蹤。 當呼叫 [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) 時，每個追蹤的動畫集都會根據追蹤加權和速度進行混合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
