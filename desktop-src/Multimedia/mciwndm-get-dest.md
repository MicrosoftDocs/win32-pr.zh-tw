---
title: 'MCIWNDM_GET_DEST 訊息 (Vfw .h) '
description: MCIWNDM \_ 取得目的地訊息會抓取在 \_ 播放期間用來縮放或延展 AVI 檔案影像的目的矩形座標。 您可以使用 MCIWndGetDest 宏明確地傳送此訊息。
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a6326485bece572b03ceeca687ca4468b6d866c25c738c32d13763fd0931a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802902"
---
# <a name="mciwndm_get_dest-message"></a>MCIWNDM \_ 取得 \_ 目的地訊息

**MCIWNDM \_ 取得 \_** 目的地訊息會抓取在播放期間用來縮放或延展 AVI 檔案影像的目的矩形座標。 您可以使用 [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) 宏明確地傳送此訊息。


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*中國*
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，用來傳回目的地矩形的座標。

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

[**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

