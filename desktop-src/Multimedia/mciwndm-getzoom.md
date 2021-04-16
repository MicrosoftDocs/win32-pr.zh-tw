---
title: 'MCIWNDM_GETZOOM 訊息 (Vfw .h) '
description: MCIWNDM \_ GETZOOM 訊息會抓取 MCI 裝置所使用的目前縮放值。 您可以使用 MCIWndGetZoom 宏明確地傳送此訊息。
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464981"
---
# <a name="mciwndm_getzoom-message"></a>MCIWNDM \_ GETZOOM 訊息

**MCIWNDM \_ GETZOOM** 訊息會抓取 MCI 裝置所使用的目前縮放值。 您可以使用 [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回與 [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)搭配使用的最新值。

## <a name="remarks"></a>備註

傳回值100表示影像未縮放。 值為200表示影像會放大至其原始大小的兩倍。 值為50表示影像縮減為其原始大小的一半。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)
</dt> </dl>

 

 





