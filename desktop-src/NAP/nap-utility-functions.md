---
title: NAP 公用程式函式
description: 下列公用程式函數支援 NAP API。
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672732"
---
# <a name="nap-utility-functions"></a>NAP 公用程式函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

下列公用程式函數支援 NAP API。

NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (CoTaskMemAlloc 和 CoTaskMemFree) 。

-   IN 參數：由呼叫端配置及釋放。
-   由被呼叫端所配置的 OUT 參數（由呼叫者使用 CoTaskMem 釋放） \* () 
-   IN/OUT 參數（由呼叫端配置）由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 CoTaskMem \* () 

在 FreeXxx () 函式中，也會釋放所有內嵌指標。

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**FreeConnections**](freeconnections-func.md)
-   [**FreeCountedString**](freecountedstring-func.md)
-   [**FreeFixupInfo**](freefixupinfo-func.md)
-   [**FreeIsolationInfo**](freeisolationinfo-func.md)
-   [**FreeIsolationInfoEx**](freeisolationinfoex.md)
-   [**FreeNapComponentRegistrationInfoArray**](freenapcomponentregistrationinfoarray-func.md)
-   [**FreeNetworkSoH**](freenetworksoh-func.md)
-   [**FreePrivateData**](freeprivatedata-func.md)
-   [**FreeSoH**](freesoh-func.md)
-   [**FreeSoHAttributeValue**](freesohattributevalue-func.md)
-   [**FreeSystemHealthAgentState**](freesystemhealthagentstate-func.md)
-   [**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
-   [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)

 

 




