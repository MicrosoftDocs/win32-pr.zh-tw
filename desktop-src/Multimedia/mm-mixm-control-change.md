---
title: 'MM_MIXM_CONTROL_CHANGE 訊息 (Mmsystem .h) '
description: '\_MIXM \_ 控制項 \_ 變更訊息是由混音器裝置傳送，以通知應用程式，與音訊行相關聯的控制項狀態已變更。 應用程式應該針對指定的控制項重新整理其顯示和快取的值。'
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44305a5a441e4d12a1b3f43029ae3a41f7642c13b15a50f74a1acab158c2ed58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807178"
---
# <a name="mm_mixm_control_change-message"></a>MM \_ MIXM \_ 控制項 \_ 變更訊息

**\_ MIXM \_ 控制項 \_ 變更** 訊息是由混音器裝置傳送，以通知應用程式，與音訊行相關聯的控制項狀態已變更。 應用程式應該針對指定的控制項重新整理其顯示和快取的值。


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

混音器裝置的控制碼 (**HMIXER** 傳送通知訊息的) 。

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

已變更狀態之混音器控制項的控制項識別碼。 此識別碼與 **mixerGetLineControls** 函數所傳回之 **MIXERCONTROL** 結構的 **dwControlID** 成員相同。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式必須開啟混音器裝置，並指定要接收 **MM \_ MIXM \_ 控制項 \_ 變更** 訊息的回呼視窗。

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

 

 





