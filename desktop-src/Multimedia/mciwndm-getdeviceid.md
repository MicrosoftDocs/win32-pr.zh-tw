---
title: 'MCIWNDM_GETDEVICEID 訊息 (Vfw .h) '
description: MCIWNDM \_ GETDEVICEID 訊息會抓取目前開啟之 MCI 裝置的識別碼，以搭配 mciSendCommand 函式使用。 您可以使用 MCIWndGetDeviceID 宏明確地傳送此訊息。
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024705"
---
# <a name="mciwndm_getdeviceid-message"></a>MCIWNDM \_ GETDEVICEID 訊息

**MCIWNDM \_ GETDEVICEID** 訊息會抓取目前開啟之 MCI 裝置的識別碼，以搭配 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函式使用。 您可以使用 [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回裝置識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

