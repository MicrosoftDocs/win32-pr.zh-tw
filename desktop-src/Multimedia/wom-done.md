---
title: 'WOM_DONE 訊息 (Mmsystem .h) '
description: '\_當指定的輸出緩衝區傳回給應用程式時，WOM 完成的訊息會傳送到波形音訊輸出回呼函式。'
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE message Windows 多媒體
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093975"
---
# <a name="wom_done-message"></a>WOM \_ 完成訊息

當指定的輸出緩衝區傳回給應用程式時， **WOM \_ 完成** 的訊息會傳送到波形音訊輸出回呼函式。 當應用程式被播放時，或呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式的結果，會將緩衝區傳回給應用程式。


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

識別緩衝區之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構的指標。

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
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

 

