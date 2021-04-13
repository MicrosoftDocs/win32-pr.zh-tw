---
title: DODownloadState 列舉
description: 指定目前下載狀態的識別碼，這是 **DO_DOWNLOAD_STATUS** 結構的一部分。
keywords:
- DODownloadState 列舉，DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509087"
---
# <a name="dodownloadstate-enumeration"></a>DODownloadState 列舉

**DODownloadState** 列舉會指定目前下載狀態的識別碼，這是 **DO_DOWNLOAD_STATUS** 結構的一部分。

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>常數

| 需求 | 值 |
|-|-|
| DODownloadState_Created | 已建立下載物件，但尚未啟動。 |
| DODownloadState_Transferring | 下載正在進行中。 |
| DODownloadState_Transferred | 下載已傳送，而且可以藉由下載檔案的另一部分來重新開機。 |
| DODownloadState_Finalized | 下載已完成，無法再次啟動。 |
| DODownloadState_Aborted | 下載已中止。 |
| DODownloadState_Paused | 下載已隨選暫停，或因為暫時性錯誤而暫停。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DeliveryOptimizationDownloadTypes。h |
