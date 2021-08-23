---
title: 'ICM_COMPRESS 訊息 (Vfw .h) '
description: ICM \_ 壓縮訊息會通知視訊壓縮驅動程式，將資料框架壓縮成應用程式定義的緩衝區。
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678468"
---
# <a name="icm_compress-message"></a>ICM \_壓縮訊息

**ICM \_ 壓縮** 訊息會通知視訊壓縮驅動程式，將資料框架壓縮成應用程式定義的緩衝區。


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*Icc*
</dt> <dd>

[**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)結構的指標。 下列結構的成員會指定壓縮參數： **lpbiInput**、 **lpInput**、 **lpbiOutput**、 **lpOutput**、 **lpbiPrev**、 **lpPrev**、 **lpckid**、 **lpdwFlags**、 **dwFrameSize** 和 **dwQuality**。 驅動程式也應該使用與 **LpbiOutput** **ICCOMPRESS** 相關聯之 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的 **biSizeImage** 成員，以傳回壓縮框架的大小。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

