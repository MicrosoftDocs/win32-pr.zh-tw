---
title: 建立變數系結清單
description: SnmpCreateVbl 函式會建立新的變數系結清單。
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2530b59524375ad6413ff9aa1416db8e25ee3641136284cb4a0f70795e388a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009576"
---
# <a name="creating-a-variable-binding-list"></a>建立變數系結清單

[**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)函式會建立新的變數系結清單。 如果 WinSNMP 應用程式指定變數名稱和值，此函式會建立清單，並新增名稱和值做為清單中的第一個專案。 如果應用程式為變數名稱指定 **Null** ，則函式會建立空的清單。

若要複製變數系結清單，請呼叫 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) 函數。 此函式會建立新的變數系結清單，並使用來源變數系結清單中的資料複本來初始化新的清單。

[**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)函式和 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)函式會為新的變數系結清單配置任何必要的記憶體。 WinSNMP 應用程式必須釋放與這些清單相關聯的資源。 建議應用程式藉由比對 [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) 和 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) 的每個呼叫，並在適當的情況下使用 [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) 函式來釋放已配置的記憶體，以進行這項作業。

 

 




