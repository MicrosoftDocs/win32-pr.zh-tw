---
title: 'MPRESOURCE_STATS 結構 (MpClient .h) '
description: 與資源相關的統計資料。
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS 結構舊版 Windows 環境功能
- PMPRESOURCE_STATS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465936"
---
# <a name="mpresource_stats-structure"></a>MPRESOURCE \_ 統計結構

與資源相關的統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>成員

<dl> <dt>

**PPMProgress**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

每百萬個)  (部分掃描的大約進度。 如果無法使用進度資訊，請將設定為 **MPPROGRESS \_ 無效** 。

</dd> <dt>

**ProcessCount**
</dt> <dd>

類型： **UINT64**

</dd> <dd>

掃描的進程數目。

</dd> <dt>

**FileCount**
</dt> <dd>

類型： **UINT64**

</dd> <dd>

掃描的檔案數目。

</dd> <dt>

**FileBytesCount**
</dt> <dd>

類型： **UINT64**

</dd> <dd>

掃描檔案的位元組數目。

</dd> <dt>

**RegKeyCount**
</dt> <dd>

類型： **UINT64**

</dd> <dd>

掃描的 RegKeys 數目。

</dd> <dt>

**已保留**
</dt> <dd>

類型： **UINT64 \[ 4 \]**

</dd> <dd>

保留供日後使用的欄位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





