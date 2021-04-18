---
title: 'MCIWNDM_GETVOLUME 訊息 (Vfw .h) '
description: MCIWNDM \_ GETVOLUME 訊息會抓取 MCI 裝置目前的磁片區設定。 您可以使用 MCIWndGetVolume 宏明確地傳送此訊息。
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385194"
---
# <a name="mciwndm_getvolume-message"></a>MCIWNDM \_ GETVOLUME 訊息

**MCIWNDM \_ GETVOLUME** 訊息會抓取 MCI 裝置目前的磁片區設定。 您可以使用 [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回目前的磁片區設定。 預設值為 1000。 較高的值表示較大的磁片區，較低的值表示更快的磁片

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





