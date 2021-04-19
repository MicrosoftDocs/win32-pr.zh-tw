---
title: 'WIM_DATA 訊息 (Mmsystem .h) '
description: '\_當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 WIM 資料訊息傳送至指定的波形-音訊輸入回撥函式。'
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966529"
---
# <a name="wim_data-message"></a>WIM \_ 資料訊息

當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 **WIM \_ 資料** 訊息傳送至指定的波形-音訊輸入回撥函式。 當緩衝區已滿或呼叫 [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) 函數之後，就可以傳送訊息。


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

[**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的指標，識別包含資料的緩衝區。

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

傳回的緩衝區可能不完整。 您可以使用 *lpwvhdr* 所指定之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwBytesRecorded** 成員，判斷記錄至傳回之緩衝區的位元組數目。

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

 

