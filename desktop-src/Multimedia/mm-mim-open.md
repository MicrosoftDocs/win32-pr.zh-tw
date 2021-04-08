---
title: 'MM_MIM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 當開啟 MIDI 輸入裝置時，會將 MM MIM 開啟訊息傳送至視窗。'
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- MM_MIM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843040"
---
# <a name="mm_mim_open-message"></a>MM \_ MIM \_ 開啟訊息

當開啟 MIDI 輸入裝置時，會將 **MM \_ MIM \_ 開啟** 訊息傳送至視窗。


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

開啟之 MIDI 輸入裝置的控制碼。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

保護請勿使用。

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

[樂器數位介面 (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

 





