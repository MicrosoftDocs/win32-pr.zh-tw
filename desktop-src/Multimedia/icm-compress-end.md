---
title: 'ICM_COMPRESS_END 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 結束訊息會通知視訊壓縮驅動程式，以結束壓縮和配置給壓縮的可用資源。 您可以使用 ICCompressEnd 宏明確地傳送此訊息。
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END 訊息 Windows 多媒體
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
ms.openlocfilehash: 9c320190da37d286db1c20329a849ea09ac6d915087e9d3bdbb2333d31cec3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785038"
---
# <a name="icm_compress_end-message"></a>ICM \_壓縮 \_ 結束訊息

**ICM \_ 壓縮 \_ 結束** 訊息會通知視訊壓縮驅動程式，以結束壓縮和配置給壓縮的可用資源。 您可以使用 [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) 宏明確地傳送此訊息。


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

bc-vcm-lvm-hyperv 會儲存最近 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md)訊息的設定。 **ICM \_壓縮 \_ BEGIN** 和 **ICM \_ 壓縮 \_ END** 不會進行嵌套。 如果您的驅動程式收到 ICM 壓縮在使用 **ICM \_ 壓縮 \_ 結束** 之前停止壓縮，則應該以新的參數重新開機壓縮。 **\_ \_**

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

 

 





