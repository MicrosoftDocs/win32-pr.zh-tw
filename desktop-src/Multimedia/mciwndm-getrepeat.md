---
title: 'MCIWNDM_GETREPEAT 訊息 (Vfw .h) '
description: MCIWNDM \_ GETREPEAT 訊息會判斷是否已啟用連續播放。 您可以使用 MCIWndGetRepeat 宏明確地傳送此訊息。
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093999"
---
# <a name="mciwndm_getrepeat-message"></a>MCIWNDM \_ GETREPEAT 訊息

**MCIWNDM \_ GETREPEAT** 訊息會判斷是否已啟用連續播放。 您可以使用 [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果啟用連續播放則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





