---
description: 設定追蹤速度。 追蹤速度類似于用來加速播放播放軌或減緩播放速度的乘數。
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'ID3DXAnimationController：： SetTrackSpeed 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323359"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a>ID3DXAnimationController：： SetTrackSpeed 方法

設定追蹤速度。 追蹤速度類似于用來加速播放播放軌或減緩播放速度的乘數。

## <a name="syntax"></a>語法


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要設定速度的曲目識別碼。

</dd> <dt>

*速度* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

新的速度。

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

 

 
