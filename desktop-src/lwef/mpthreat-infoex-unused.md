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
ms.openlocfilehash: 8def13a6f6aff010b9854055abd4636d19f77ef1f0e9867ec5e4d7562baff4f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601098"
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





