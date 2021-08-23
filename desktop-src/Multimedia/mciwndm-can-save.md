---
title: 'MCIWNDM_CAN_SAVE 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 儲存訊息，以判斷 MCI 裝置是否可以儲存資料。 您可以使用 MCIWndCanSave 宏明確地傳送此訊息。
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccab622381208b8213414ed8b156a84e431afffc55acdf2323b0c0a2d31014f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429628"
---
# <a name="mciwndm_can_save-message"></a>MCIWNDM \_ 可以 \_ 儲存訊息

**MCIWNDM \_ 可以 \_ 儲存** 訊息，以判斷 MCI 裝置是否可以儲存資料。 您可以使用 [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) 宏明確地傳送此訊息。


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果裝置支援儲存，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





