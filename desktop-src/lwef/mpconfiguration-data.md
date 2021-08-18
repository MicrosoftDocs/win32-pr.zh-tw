---
title: 'MPCONFIGURATION_DATA 結構 (MpClient .h) '
description: 包含設定變更的相關資料，包括舊值和新值。
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA 結構舊版 Windows 環境功能
- PMPCONFIGURATION_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cb4d2e35d1b471ef92fb976535bb1e6ed733e2f29ebf86d357f722904514c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114578"
---
# <a name="mpconfiguration_data-structure"></a>MPCONFIGURATION \_ 資料結構

包含設定變更的相關資料，包括舊值和新值。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ConfigurationName**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

變更的設定名稱。

</dd> <dt>

**DataType**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

使用的資料類型。

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

先前資料的大小（以位元組為單位）。

</dd> <dt>

**pPreviousData**
</dt> <dd>

類型：**位元組 \***

</dd> <dd>

先前資料的指標。

</dd> <dt>

**CurrentDataSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

新資料的大小（以位元組為單位）。

</dd> <dt>

**pCurrentData**
</dt> <dd>

類型：**位元組 \***

</dd> <dd>

新資料的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





