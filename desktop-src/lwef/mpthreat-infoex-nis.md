---
title: 'MPTHREAT_INFOEX_NIS 結構 (MpClient .h) '
description: 包含 NIS 特定的資訊。
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS 結構舊版 Windows 環境功能
- PMPTHREAT_INFOEX_NIS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025044"
---
# <a name="mpthreat_infoex_nis-structure"></a>MPTHREAT \_ INFOEX \_ NIS 結構

包含 NIS 特定的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a>成員

<dl> <dt>

**SourceIP**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd></dd> <dt>

**DestinationIP**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd></dd> <dt>

**dwSourceport**
</dt> <dd>

類型： **DWORD**

</dd> <dd></dd> <dt>

**dwDestinationport**
</dt> <dd>

類型： **DWORD**

</dd> <dd></dd> <dt>

**通訊協定**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd></dd> <dt>

**連結**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





