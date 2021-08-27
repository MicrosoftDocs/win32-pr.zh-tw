---
title: 'MPHEALTH_DATA 結構 (MpClient .h) '
description: 健康情況通知資料。
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA 結構舊版 Windows 環境功能
- PMPHEALTH_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb04224d38e639d053b8e20370e2b0db0dc15f44cc647e7205911362112e4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975998"
---
# <a name="mphealth_data-structure"></a>MPHEALTH \_ 資料結構

健康情況通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**dwNotificationType**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

通知的類型。

</dd> <dt>

**dwNotificationFlag**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

未使用的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





