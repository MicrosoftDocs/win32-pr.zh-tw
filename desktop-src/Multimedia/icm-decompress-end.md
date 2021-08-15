---
title: 'ICM_DECOMPRESS_END 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 結束訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 ICDecompressEnd 宏明確地傳送此訊息。
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c877afac3db0e4cf4d7c476ca3806d2acd15bdf72764549b2958490574a4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691158"
---
# <a name="icm_decompress_end-message"></a>ICM \_解壓縮 \_ 結束訊息

**ICM \_ 解壓縮 \_ 結束** 訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

驅動程式應該釋放針對 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md)訊息所配置的任何資源。

[**ICM \_解壓縮 \_ BEGIN**](icm-decompress-begin.md)和 **ICM \_ 解壓縮 \_ END** 不會被嵌套。 如果您的驅動程式收到 ICM 解壓縮在使用 **ICM \_ 解壓縮 \_ 結束** 之前停止解壓縮，則應該以新的參數重新開機解壓縮。 **\_ \_**

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

 

 





