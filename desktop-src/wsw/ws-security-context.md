---
title: 'WS_SECURITY_CONTEXT (WebServices) '
description: 用來參考安全性內容物件的不透明類型。
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104238"
---
# <a name="ws_security_context"></a>WS \_ 安全性 \_ 內容

用來參考 [安全性內容物件](security-context.md)的不透明類型。


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>備註

此物件不是安全線程。 如需詳細資訊，請參閱 [執行緒安全性](thread-safety.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>WebServices。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[安全性內容](security-context.md)
</dt> <dt>

[執行緒安全性](thread-safety.md)
</dt> </dl>

 

 





