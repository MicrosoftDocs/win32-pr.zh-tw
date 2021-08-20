---
title: 'ICM_COMPRESS_FRAMES_INFO 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 畫面格 \_ 資訊訊息會通知壓縮驅動程式，以設定暫止壓縮的參數。
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140909"
---
# <a name="icm_compress_frames_info-message"></a>ICM \_壓縮 \_ 框架 \_ 資訊訊息

**ICM \_ 壓縮畫面 \_ 格 \_ 資訊** 訊息會通知壓縮驅動程式，以設定暫止壓縮的參數。


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*Icf*
</dt> <dd>

[**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)結構的指標。 此 **結構** 的 **PutData** 成員不會與此訊息一起使用。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

壓縮程式可以使用此訊息來判斷在壓縮時要為每個框架配置多少空間。

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

 

 





