---
title: 'MCIWNDM_GETALIAS 訊息 (Vfw .h) '
description: MCIWNDM \_ GETALIAS 訊息會抓取用來開啟 MCI 裝置或具有 mciSendString 功能之檔案的別名。 您可以使用 MCIWndGetAlias 宏明確地傳送此訊息。
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857ea90205b5204cd7c4af19f27a420684e59543717b2689f178d97cd5a600de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137749"
---
# <a name="mciwndm_getalias-message"></a>MCIWNDM \_ GETALIAS 訊息

**MCIWNDM \_ GETALIAS** 訊息會抓取用來開啟 MCI 裝置或具有 [**mciSendString**](/previous-versions//dd757161(v=vs.85))功能之檔案的別名。 您可以使用 [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回裝置別名。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

