---
title: 'MM_WOM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 當指定的波形音訊輸出裝置開啟時，MM WOM 開啟的訊息會傳送至視窗。'
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106518"
---
# <a name="mm_wom_open-message"></a>MM \_ WOM \_ 開啟的訊息

當指定的波形音訊輸出裝置開啟時， **MM \_ WOM \_ 開啟** 的訊息會傳送至視窗。


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

開啟之裝置的控制碼。

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
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[波形音訊](waveform-audio.md)
</dt> <dt>

[波形訊息](waveform-messages.md)
</dt> </dl>

 

 





