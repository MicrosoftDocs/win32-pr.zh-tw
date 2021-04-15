---
title: 'ICM_COMPRESS_END 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 結束訊息會通知影片壓縮驅動程式，以結束壓縮和配置給壓縮的可用資源。 您可以使用 ICCompressEnd 宏明確地傳送此訊息。
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464836"
---
# <a name="icm_compress_end-message"></a>ICM \_ 壓縮 \_ 結束訊息

**ICM \_ 壓縮 \_ 結束** 訊息會通知影片壓縮驅動程式，以結束壓縮和配置給壓縮的可用資源。 您可以使用 [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) 宏明確地傳送此訊息。


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

BC-VCM-LVM-HYPERV 會儲存最近的 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md) 訊息的設定。 **ICM \_壓縮 \_ BEGIN** 和 **ICM \_ 壓縮 \_ 結束** 不會被嵌套。 如果您的驅動程式會在使用 **icm \_ 壓縮 \_ 結束** 的情況下，于壓縮停止之前收到 **icm \_ 壓縮 \_ 開始**，則應該以新的參數重新開機壓縮。

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

 

 





