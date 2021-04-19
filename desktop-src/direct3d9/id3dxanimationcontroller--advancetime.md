---
description: 將網格繪製到動畫，並以指定的數量前進全域動畫時間。
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'ID3DXAnimationController：： AdvanceTime 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988215"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>ID3DXAnimationController：： AdvanceTime 方法

將網格繪製到動畫，並以指定的數量前進全域動畫時間。

## <a name="syntax"></a>語法


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TimeDelta* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

前進全域動畫時間的金額（以秒為單位）。 TimeDelta 值不能為負數或零。

</dd> <dt>

*pCallbackHandler* \[在\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

使用者定義動畫回呼處理常式介面的指標， [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md)。

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

 

 
