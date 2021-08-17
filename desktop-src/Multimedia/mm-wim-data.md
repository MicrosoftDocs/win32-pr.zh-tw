---
title: 'MM_WIM_DATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 MM WIM 資料訊息傳送至視窗。 當緩衝區已滿或呼叫 waveInReset 函數之後，就可以傳送此訊息。'
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b209e59032c0da4c875a316008c889cf064ae7d8bc48f5c621125a06582673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065468"
---
# <a name="mm_wim_data-message"></a>MM \_ WIM \_ 資料訊息

當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 **MM \_ WIM \_ 資料** 訊息傳送至視窗。 當緩衝區已滿或呼叫 [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) 函數之後，就可以傳送此訊息。


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

接收資料之波形音訊輸入裝置的控制碼。

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

[**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的指標，識別包含資料的緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

傳回的緩衝區可能不完整。 您可以使用 *lParam* 所指定之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwBytesRecorded** 成員，判斷記錄至傳回之緩衝區的位元組數目。

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

 

