---
title: 開啟和關閉 WinSNMP 應用程式
description: 在呼叫任何其他的 WinSNMP 函數之前，必須先成功呼叫 SnmpStartup 函式。
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021774"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>開啟和關閉 WinSNMP 應用程式

在呼叫任何其他的 WinSNMP 函數之前，必須先成功呼叫 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) 函式。 **SnmpStartup** 函式可讓 Microsoft WinSNMP 實行執行初始化程式。 函式也會將執行所支援的 WinSNMP API 版本、支援的 SNMP 通訊層級，以及執行的預設轉譯和重新傳輸模式，傳回給應用程式。

當應用程式不再需要執行程式的服務時，必須呼叫 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) 函式。 即使 **SnmpCleanup** 可讓實施解除配置配置給應用程式的所有資源，建議應用程式先針對每個開啟的 WinSNMP 會話呼叫 [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) 函式一次，以將執行效能最大化。 在終止應用程式之前，必須先呼叫 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) 作為最後的 WinSNMP 函數。

 

 




