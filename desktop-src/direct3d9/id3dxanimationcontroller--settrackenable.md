---
description: 啟用或停用動畫控制器中的軌跡。
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'ID3DXAnimationController：： SetTrackEnable 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61078a40e13ee1422c29de091e1758444e2bafa1586bb443e763e50d57457ad5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026578"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>ID3DXAnimationController：： SetTrackEnable 方法

啟用或停用動畫控制器中的軌跡。

## <a name="syntax"></a>語法


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要混合之追蹤的識別碼。

</dd> <dt>

*啟用* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

啟用值。 設定為 **TRUE** 可在控制器中啟用此追蹤，或設為 **FALSE** 以防止其混合。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

若要混用追蹤與其他曲目，啟用旗標必須設定為 **TRUE**。 相反地，將旗標設定為 **FALSE** 將會防止追蹤與其他曲目混合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
