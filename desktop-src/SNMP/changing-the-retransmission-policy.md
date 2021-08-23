---
title: 變更重新傳輸原則
description: Microsoft 的 WinSNMP 實行提供重新傳輸原則支援，方法是為資料庫中的 WinSNMP 應用程式儲存超時值和重試計數。
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed160de40b300d1b2430304b7a487f4544fee9a13db6049d1d837958276da8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009766"
---
# <a name="changing-the-retransmission-policy"></a>變更重新傳輸原則

Microsoft 的 WinSNMP 實行提供重新傳輸原則支援，方法是為資料庫中的 WinSNMP 應用程式儲存超時值和重試計數。 此實值會儲存個別目的地實體的值。 此實作為一開始會提供這些專案的預設值，但應用程式可以加入或修改個別實體的值。

呼叫 [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) 和 [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) 函數會傳回特定目的地實體的超時和重試計數值。 若要變更超時值，則必須呼叫 [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) 函式的 WinSNMP 應用程式。 若要變更重試計數值，應用程式必須呼叫 [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) 函數。 更新的設定會影響目的地實體的新 SNMP 訊息要求。

 

 




