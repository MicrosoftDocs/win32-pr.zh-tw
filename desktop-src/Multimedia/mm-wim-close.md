---
title: 'MM_WIM_CLOSE 訊息 (Mmsystem .h) '
description: '\_ \_ 當波形音訊輸入裝置關閉時，會將 MM WIM 關閉訊息傳送至視窗。 傳送此訊息之後，裝置控制碼已不再有效。'
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506311f9938198e2ceb99646670c954eaa433825855e31c036241df6be1b2491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807108"
---
# <a name="mm_wim_close-message"></a>MM \_ WIM \_ 關閉訊息

當波形音訊輸入裝置關閉時，會將 **MM \_ WIM \_ 關閉** 訊息傳送至視窗。 傳送此訊息之後，裝置控制碼已不再有效。


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

已關閉波形音訊輸入裝置的控制碼。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[波形音訊](waveform-audio.md)
</dt> <dt>

[波形訊息](waveform-messages.md)
</dt> </dl>

 

 





