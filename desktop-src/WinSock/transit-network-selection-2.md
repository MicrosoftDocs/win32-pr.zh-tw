---
description: 此區段會列出用於傳輸網路選項的值。
ms.assetid: cafb47c0-73ff-47e4-8968-c065c821e646
title: 傳輸網路選取範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d293c9160019ae95ddeda483ea9001b37c45afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001409"
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

 

 



