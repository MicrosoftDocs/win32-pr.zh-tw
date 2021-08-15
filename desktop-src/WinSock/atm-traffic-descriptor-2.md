---
description: 本節列出 ATM 流量描述項。
ms.assetid: 8d15af95-2003-416e-b3b0-a9201972a899
title: ATM 流量描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cd4ec218f8f3a6719bb71a1eb2d6ef11179ca44878641aaf25906e6eae1dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097918"
---
# <a name="atm-traffic-descriptor"></a>ATM 流量描述項

本節列出 ATM 流量描述項。

``` syntax
typedef struct {
    ULONG PeakCellRate_CLP0;
    ULONG PeakCellRate_CLP01;
    ULONG SustainableCellRate_CLP0;
    ULONG SustainableCellRate_CLP01;
    ULONG MaxBurstSize_CLP0;
    ULONG MaxBurstSize_CLP01;
    BOOL  Tagging;
} ATM_TD;

typedef struct {
    ATM_TD Forward;
    ATM_TD Backward;
    BOOL   BestEffort;
} ATM_TRAFFIC_DESCRIPTOR_IE;
```

 

 



