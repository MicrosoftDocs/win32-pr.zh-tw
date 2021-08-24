---
title: DODownloadCostPolicy 列舉
description: 指定與 **DODownloadProperty_CostPolicy** 屬性相關聯之成本原則選項的識別碼。
keywords:
- DODownloadCostPolicy 列舉，DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 763042ed6d0df6fa287fbe66d23528a199a73041cb3500c6a2812e6db86cb698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677878"
---
# <a name="dodownloadcostpolicy-enumeration"></a>DODownloadCostPolicy 列舉

**DODownloadCostPolicy** 列舉會指定與 **DODownloadProperty_CostPolicy** 屬性相關聯之成本原則選項的識別碼。

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>常數

| 需求 | 值 |
|-|-|
| DODownloadCostPolicy_Always | 無論成本為何，都可執行下載。 |
| DODownloadCostPolicy_Unrestricted | 除非強加成本或流量限制，否則會執行下載。 |
| DODownloadCostPolicy_Standard | 除非沒有額外費用或接近耗盡的情況，否則請下載執行。 |
| DODownloadCostPolicy_NoRoaming | 下載執行，除非連線受限於漫遊的附加費。 |
| DODownloadCostPolicy_NoSurcharge | 下載執行，除非有額外費用。 |
| DODownloadCostPolicy_NoCellular | 除非網路在行動電話上，否則會執行下載。 |

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DeliveryOptimizationDownloadTypes。h |
