---
title: 'MCIWNDM_CAN_EJECT 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 退出訊息，以判斷 MCI 裝置是否可以退出媒體。 您可以使用 MCIWndCanEject 宏明確地傳送此訊息。
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde4c9fec3972fe0e22b0a562454e1ef680e9ccae3851c272d28468fc2c91f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429668"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ 可以 \_ 退出訊息

**MCIWNDM \_ 可以 \_ 退出** 訊息，以判斷 MCI 裝置是否可以退出媒體。 您可以使用 [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) 宏明確地傳送此訊息。


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果裝置可以退出媒體，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





