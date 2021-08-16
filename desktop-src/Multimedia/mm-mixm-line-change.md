---
title: 'MM_MIXM_LINE_CHANGE 訊息 (Mmsystem .h) '
description: '\_MIXM \_ 線路 \_ 變更訊息會由混音器裝置傳送，以通知應用程式，指定裝置上的音訊行狀態已變更。 應用程式應該針對指定的音訊行重新整理其顯示和快取的值。'
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3bd1c122d5e0cf62aa39266da547cd3701e43e6afbf01b853c7d24040504d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373575"
---
# <a name="mm_mixm_line_change-message"></a>MM \_ MIXM \_ 行 \_ 變更訊息

**\_ MIXM \_ 線路 \_ 變更** 訊息會由混音器裝置傳送，以通知應用程式，指定裝置上的音訊行狀態已變更。 應用程式應該針對指定的音訊行重新整理其顯示和快取的值。


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

傳送通知訊息的混音器裝置的控制碼。

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

已變更狀態之音訊行的行識別碼。 此識別碼與 **mixerGetLineInfo** 函數所傳回之 **MIXERLINE** 結構的 **dwLineID** 成員相同。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式必須開啟混音器裝置，並指定要接收 **MM \_ MIXM \_ 線路 \_ 變更** 訊息的回呼視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[音訊 Mixers](audio-mixers.md)
</dt> <dt>

[音訊 Mixer 訊息](audio-mixer-messages.md)
</dt> </dl>

 

 





