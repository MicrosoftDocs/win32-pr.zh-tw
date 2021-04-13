---
title: 'MCIWNDM_EJECT 訊息 (Vfw .h) '
description: MCIWNDM \_ 退出訊息會將命令傳送至 MCI 裝置，以將其媒體退出。 您可以使用 MCIWndEject 宏明確地傳送此訊息。
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384122"
---
# <a name="mciwndm_eject-message"></a>MCIWNDM \_ 退出訊息

**MCIWNDM \_ 退出** 訊息會將命令傳送至 MCI 裝置，以將其媒體退出。 您可以使用 [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) 宏明確地傳送此訊息。


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





