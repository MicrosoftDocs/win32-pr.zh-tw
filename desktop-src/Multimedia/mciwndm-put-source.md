---
title: 'MCIWNDM_PUT_SOURCE 訊息 (Vfw .h) '
description: MCIWNDM \_ PUT \_ 來源訊息會重新定義來源矩形的座標，在播放期間用於裁剪 AVI 檔案的影像。 您可以使用 MCIWndPutSource 宏明確地傳送此訊息。
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c21e11142a1b47a8984712de664151b686cfa3c3cb9bf153dcbc2a23fa459c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807778"
---
# <a name="mciwndm_put_source-message"></a>MCIWNDM \_ PUT \_ 來源訊息

**MCIWNDM \_ PUT \_ 來源** 訊息會重新定義來源矩形的座標，在播放期間用於裁剪 AVI 檔案的影像。 您可以使用 [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) 宏明確地傳送此訊息。


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*中國*
</dt> <dd>

[矩形](/previous-versions//ms536136(v=vs.85))結構的指標，其中包含來源矩形的座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

