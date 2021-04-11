---
title: 'MPTHREAT_INFOEX_UNUSED 結構 (MpClient .h) '
description: 非行為修改類型威脅的虛擬結構。
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED 結構舊版 Windows 環境功能
- PMPTHREAT_INFOEX_UNUSED 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104537"
---
# <a name="mpthreat_infoex_unused-structure"></a>MPTHREAT \_ INFOEX \_ 未使用的結構

非行為修改類型威脅的虛擬結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a>成員

<dl> <dt>

**dwNone**
</dt> <dd>

類型： **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





