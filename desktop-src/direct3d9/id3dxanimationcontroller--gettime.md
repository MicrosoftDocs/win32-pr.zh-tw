---
description: 取得全域動畫時間。
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController：： GetTime 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6241bbd8c447889a4718369feabf8f26dacc73c58b8e6826c1797d0639422fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987828"
---
# <a name="id3dxanimationcontrollergettime-method"></a>ID3DXAnimationController：： GetTime 方法

取得全域動畫時間。

## <a name="syntax"></a>語法


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

傳回全域動畫時間。

## <a name="remarks"></a>備註

動畫的設計是使用本機動畫時間，並使用 [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)混合到全球時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
