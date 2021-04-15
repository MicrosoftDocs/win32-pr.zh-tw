---
title: 'MCIWNDM_CAN_RECORD 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 記錄訊息，判斷 MCI 裝置是否支援錄製。 您可以使用 MCIWndCanRecord 宏明確地傳送此訊息。
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466644"
---
# <a name="mciwndm_can_record-message"></a>MCIWNDM \_ 可以 \_ 記錄訊息

**MCIWNDM \_ 可以 \_ 記錄** 訊息，判斷 MCI 裝置是否支援錄製。 您可以使用 [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) 宏明確地傳送此訊息。


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果裝置支援錄製則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





