---
title: 'MPCOMPONENT_STATUS 結構 (MpClient .h) '
description: 元件狀態資訊。
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS 結構舊版 Windows 環境功能
- PMPCOMPONENT_STATUS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747796"
---
# <a name="mpcomponent_status-structure"></a>MPCOMPONENT \_ 狀態結構

元件狀態資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**fEnable**
</dt> <dd>

類型： **BOOL**

</dd> <dd>

元件的狀態。

</dd> <dt>

**hResult**
</dt> <dd>

類型： **HRESULT**

</dd> <dd>

與狀態相關聯的成功或失敗代碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





