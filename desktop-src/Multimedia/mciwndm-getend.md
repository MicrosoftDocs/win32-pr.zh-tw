---
title: 'MCIWNDM_GETEND 訊息 (Vfw .h) '
description: MCIWNDM \_ GETEND 訊息會抓取 MCI 裝置或檔案的內容結尾位置。 您可以使用 MCIWndGetEnd 宏明確地傳送此訊息。
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880b1a464d671ca57e1955d4131776a999d1fb6bd8f17ad5d08139abc64a757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137729"
---
# <a name="mciwndm_getend-message"></a>MCIWNDM \_ GETEND 訊息

**MCIWNDM \_ GETEND** 訊息會抓取 MCI 裝置或檔案的內容結尾位置。 您可以使用 [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回目前時間格式的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





