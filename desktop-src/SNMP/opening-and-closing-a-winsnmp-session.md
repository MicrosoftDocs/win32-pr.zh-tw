---
title: 開啟和關閉 WinSNMP 會話
description: 若要開啟會話，應用程式會呼叫 SnmpCreateSession 函數。
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021772"
---
# <a name="opening-and-closing-a-winsnmp-session"></a>開啟和關閉 WinSNMP 會話

若要開啟會話，應用程式會呼叫 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) 函數。 如果函式順利完成，Microsoft WinSNMP 執行會開啟會話，而此函式會以 **HSNMP \_ 會話** 控制碼的形式傳回會話識別碼。 所有傳回控制碼變數的 WinSNMP 函數都會包含會話識別碼作為輸入參數。 這可讓實作為使用控制碼，有效率地管理工作階段層級的資源。

應用程式一次可以有多個會話開啟。 應用程式內的多個會話可以共用控制碼變數。

如果由於資源限制而無法開啟會話，則 \_ 當應用程式呼叫 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)時，它會傳回 SNMPAPI 失敗。 如果應用程式接著呼叫 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 函數，它會傳回 SNMPAPI \_ 配置 \_ 錯誤。

[**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)函式的呼叫可讓實作為釋放任何剩餘的資源，並關閉會話。

如需詳細資訊，請參閱 [資源控制碼物件](resource-handle-objects.md) 和 [WinSNMP 會話](winsnmp-sessions.md)。

 

 




