---
description: 本節列出 ATM 流量描述項。
ms.assetid: 8d15af95-2003-416e-b3b0-a9201972a899
title: ATM 流量描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb841cea1cacd3a613162a7e7da779872eb7ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113108"
---
# <a name="atm-traffic-descriptor"></a><span data-ttu-id="ee2c5-103">ATM 流量描述項</span><span class="sxs-lookup"><span data-stu-id="ee2c5-103">ATM Traffic Descriptor</span></span>

<span data-ttu-id="ee2c5-104">本節列出 ATM 流量描述項。</span><span class="sxs-lookup"><span data-stu-id="ee2c5-104">This section lists the ATM traffic descriptor.</span></span>

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

 

 



