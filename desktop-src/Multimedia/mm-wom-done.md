---
title: 'MM_WOM_DONE 訊息 (Mmsystem .h) '
description: '\_ \_ 當給定的輸出緩衝區傳回給應用程式時，會將 MM WOM 完成訊息傳送至視窗。 當應用程式被播放時，或呼叫 waveOutReset 函式的結果，會將緩衝區傳回給應用程式。'
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225ba32f780831ab8b40f487a312a940219abc2e976be75a4e903648344afc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065458"
---
# <a name="mm_wom_done-message"></a>MM \_ WOM \_ 完成訊息

當給定的輸出緩衝區傳回給應用程式時，會將 **MM \_ WOM \_ 完成** 訊息傳送至視窗。 當應用程式被播放時，或呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式的結果，會將緩衝區傳回給應用程式。


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

播放緩衝區之波形音訊輸出裝置的控制碼。

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

識別緩衝區之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構的指標。

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

 

