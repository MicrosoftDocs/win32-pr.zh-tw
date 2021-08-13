---
title: 'MCIWNDM_CAN_RECORD 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 記錄訊息，判斷 MCI 裝置是否支援錄製。 您可以使用 MCIWndCanRecord 宏明確地傳送此訊息。
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD 訊息 Windows 多媒體
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
ms.openlocfilehash: 5df46ce0cbffe17f890e50159a13a93192e67f60e323d6ba711bee6af7ac3f79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429648"
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

 

 





