---
title: 'MPRESERVED_DATA 結構 (MpClient .h) '
description: 保留的通知資料。
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA 結構舊版 Windows 環境功能
- PMPRESERVED_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747652"
---
# <a name="mpreserved_data-structure"></a>MPRESERVED \_ 資料結構

保留的通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**cbReservedData**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

保留資料的大小（以位元組為單位）。

</dd> <dt>

**pbReservedData**
</dt> <dd>

類型：**位元組 \***

</dd> <dd>

保留資料的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





