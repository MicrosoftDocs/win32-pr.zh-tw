---
title: 'ICM_DECOMPRESSEX_END 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX \_ 終端訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 ICDecompressExEnd 宏明確地傳送此訊息。
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509151"
---
# <a name="icm_decompressex_end-message"></a>ICM \_ DECOMPRESSEX \_ 結束訊息

**ICM \_ DECOMPRESSEX \_ 終端** 訊息會通知影片解壓縮驅動程式，以結束解壓縮和配置給解壓縮的可用資源。 您可以使用 [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

驅動程式會釋出配置給 [**ICM \_ DECOMPRESSEX \_ 開始**](icm-decompressex-begin.md) 訊息的任何資源。

[**ICM \_DECOMPRESSEX \_ BEGIN**](icm-decompressex-begin.md) 和 **ICM \_ DECOMPRESSEX \_ END** 不會被嵌套。 如果您的驅動程式收到 Icm DECOMPRESSEX 在使用 **icm \_ DECOMPRESSEX \_ END** 停止解壓縮之前 **\_ \_ 開始**，則應該以新的參數重新開機解壓縮。

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

 

 





