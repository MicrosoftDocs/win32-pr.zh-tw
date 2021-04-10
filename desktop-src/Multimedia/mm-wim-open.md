---
title: 'MM_WIM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 開啟波形音訊輸入裝置時，會將 MM WIM OPEN 訊息傳送至視窗。'
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- MM_WIM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025495"
---
# <a name="mm_wim_open-message"></a>MM \_ WIM \_ 開啟訊息

開啟波形音訊輸入裝置時，會將 **MM \_ WIM \_ OPEN** 訊息傳送至視窗。


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
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

 

 





