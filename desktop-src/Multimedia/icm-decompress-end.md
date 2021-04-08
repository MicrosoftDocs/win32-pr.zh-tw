---
title: 'ICM_DECOMPRESS_END 訊息 (Vfw .h) '
description: ICM \_ 解壓縮 \_ 結束訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 ICDecompressEnd 宏明確地傳送此訊息。
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END message Windows 多媒體
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
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686275"
---
# <a name="icm_decompress_end-message"></a>ICM \_ 解壓縮 \_ 結束訊息

**ICM \_ 解壓縮 \_ 結束** 訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

驅動程式應該釋放配置給 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息的任何資源。

[**ICM \_解壓縮 \_ 開始**](icm-decompress-begin.md) 和 **ICM \_ 解壓縮 \_ 結束** 不會被嵌套。 如果您的驅動程式在使用 **icm \_ 解壓縮 \_ 結束** 解壓縮之前收到 **icm \_ 解壓縮 \_** ，則應該以新的參數重新開機解壓縮。

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

 

 





