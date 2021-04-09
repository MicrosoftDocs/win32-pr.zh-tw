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
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685788"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





