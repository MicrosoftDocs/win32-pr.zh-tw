---
description: 此區段會列出用於傳輸網路選項的值。
ms.assetid: cafb47c0-73ff-47e4-8968-c065c821e646
title: 傳輸網路選取範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5da059e7b0d31e0496e2e10b4e7edeb887be7d08693b67848c87bcbde1b3f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559305"
---
# <a name="transit-network-selection"></a>傳輸網路選取範圍

此區段會列出用於傳輸網路選項的值。

``` syntax
#include <windows.h>
/* 
 *  values used for the TypeOfNetworkId field in struct ATM_TRANSIT_NETWORK_SELECTION_IE
 */
#define TNS_TYPE_NATIONAL           0x40

/* 
 *  values used for the NetworkIdPlan field in struct ATM_TRANSIT_NETWORK_SELECTION_IE
 */
#define TNS_PLAN_CARRIER_ID_CODE    0x01

typedef struct {
    UCHAR TypeOfNetworkId;
    UCHAR NetworkIdPlan;
    UCHAR NetworkIdLength;
    UCHAR NetworkId[1];
} ATM_TRANSIT_NETWORK_SELECTION_IE;
```

 

 



