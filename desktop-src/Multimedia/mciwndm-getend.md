---
title: 'MCIWNDM_GETEND 訊息 (Vfw .h) '
description: MCIWNDM \_ GETEND 訊息會抓取 MCI 裝置或檔案的內容結尾位置。 您可以使用 MCIWndGetEnd 宏明確地傳送此訊息。
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND message Windows 多媒體
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
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844224"
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

 

 





