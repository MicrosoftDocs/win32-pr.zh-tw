---
title: 'ICM_SETQUALITY 訊息 (Vfw .h) '
description: ICM \_ SETQUALITY 訊息提供的視訊壓縮驅動程式具有要在壓縮期間使用的品質等級。
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- ICM_SETQUALITY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385298"
---
# <a name="icm_setquality-message"></a>ICM \_ SETQUALITY 訊息

**ICM \_ SETQUALITY** 訊息提供的視訊壓縮驅動程式具有要在壓縮期間使用的品質等級。


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

新的品質值。 品質值的範圍是從0到10000。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 





