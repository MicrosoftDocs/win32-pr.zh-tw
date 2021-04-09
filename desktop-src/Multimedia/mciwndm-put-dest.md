---
title: 'MCIWNDM_PUT_DEST 訊息 (Vfw .h) '
description: MCIWNDM \_ PUT \_ DEST 訊息會在播放期間，重新定義用於縮放或延展 AVI 檔案影像的目的矩形座標。 您可以使用 MCIWndPutDest 宏明確地傳送此訊息。
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686270"
---
# <a name="mciwndm_put_dest-message"></a>MCIWNDM \_ PUT \_ DEST 訊息

**MCIWNDM \_ PUT \_ DEST** 訊息會在播放期間，重新定義用於縮放或延展 AVI 檔案影像的目的矩形座標。 您可以使用 [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) 宏明確地傳送此訊息。


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*中國*
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含目的地矩形的座標。

</dd> </dl>

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

[**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

