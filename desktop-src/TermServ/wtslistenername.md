---
title: 'WTSLISTENERNAME (Wtsapi32.dll) '
description: 代表遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上遠端桌面服務接聽程式的名稱。
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384953"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

代表遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上遠端桌面服務接聽程式的名稱。


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**WTSLISTENERNAMEW**
</dt> <dd>

接聽程式的 Unicode 名稱。

</dd> <dt>

**WTSLISTENERNAMEA**
</dt> <dd>

接聽程式之 ANSI 名稱的指標。

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

接聽程式的名稱。

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

接聽程式名稱的指標。

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

接聽程式的名稱。

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

接聽程式名稱的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Wtsapi32.dll。h</dt> </dl> |



 

 





