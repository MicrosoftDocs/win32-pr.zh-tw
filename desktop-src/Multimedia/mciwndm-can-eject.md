---
title: 'MCIWNDM_CAN_EJECT 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 退出訊息，以判斷 MCI 裝置是否可以退出媒體。 您可以使用 MCIWndCanEject 宏明確地傳送此訊息。
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT message Windows 多媒體
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
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686520"
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

 

 





