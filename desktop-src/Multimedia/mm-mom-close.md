---
title: 'MM_MOM_CLOSE 訊息 (Mmsystem .h) '
description: '\_ \_ 當 MIDI 輸出裝置關閉時，會將 MM MOM 關閉訊息傳送至視窗。'
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464497"
---
# <a name="mm_mom_close-message"></a>MM \_ MOM \_ 關閉訊息

當 MIDI 輸出裝置關閉時，會將 **MM \_ MOM \_ 關閉** 訊息傳送至視窗。


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

MIDI 輸出裝置的控制碼。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

保護請勿使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

傳送此訊息之後，裝置控制碼已不再有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

 





