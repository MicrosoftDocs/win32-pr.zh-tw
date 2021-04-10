---
title: 'MPSAMPLE_DATA 結構 (MpClient .h) '
description: 傳遞給範例提交回呼函數的通知資料。
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA 結構舊版 Windows 環境功能
- PMPSAMPLE_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106296"
---
# <a name="mpsample_data-structure"></a>MPSAMPLE \_ 資料結構

傳遞給範例提交回呼函數的通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSampleIndex**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

回報其提交狀態之範例專案的索引。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





