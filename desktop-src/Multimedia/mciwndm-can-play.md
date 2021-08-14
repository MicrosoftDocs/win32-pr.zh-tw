---
title: 'MCIWNDM_CAN_PLAY 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 播放訊息，判斷 MCI 裝置是否可以播放某個其他種類的資料檔或內容。 您可以使用 MCIWndCanPlay 宏明確地傳送此訊息。
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d067b01dbce8aaab7c78ab24c3d11fc5d4a3a19b9bfdb663eb653ebc0c553c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374240"
---
# <a name="mciwndm_can_play-message"></a>MCIWNDM \_ 可以 \_ 播放訊息

**MCIWNDM \_ 可以 \_ 播放** 訊息，判斷 MCI 裝置是否可以播放某個其他種類的資料檔或內容。 您可以使用 [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) 宏明確地傳送此訊息。


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果裝置支援播放資料則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





