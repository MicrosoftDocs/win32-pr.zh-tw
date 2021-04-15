---
title: 'MCIWNDM_SETZOOM 訊息 (Vfw .h) '
description: MCIWNDM \_ SETZOOM 訊息會根據縮放因數調整影片影像的大小。 這個 marco 會調整 MCIWnd 視窗的大小，同時維持固定的長寬比。 您可以使用 MCIWndSetZoom 宏明確地傳送此訊息。
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464508"
---
# <a name="mciwndm_setzoom-message"></a>MCIWNDM \_ SETZOOM 訊息

**MCIWNDM \_ SETZOOM** 訊息會根據縮放因數調整影片影像的大小。 這個 marco 會調整 MCIWnd 視窗的大小，同時維持固定的長寬比。 您可以使用 [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

以原始影像的百分比表示的縮放因數。 指定100以其所撰寫的大小顯示影像，200以在其正常大小的兩倍顯示影像，或以50顯示影像的大小為一半。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





