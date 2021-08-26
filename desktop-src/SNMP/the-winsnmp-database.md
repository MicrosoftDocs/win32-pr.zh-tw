---
title: WinSNMP 資料庫
description: Microsoft WinSNMP 執行會在資料庫中維護系統管理資訊的存放區。
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f478c9bb1c05d3a094e2a15fac0a9cef5968f245257a0702d045eb90bd2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885998"
---
# <a name="the-winsnmp-database"></a>WinSNMP 資料庫

Microsoft WinSNMP 執行會在資料庫中維護系統管理資訊的存放區。 資料庫包含下列資訊：

-   網路和版本屬性。

    此執行會使用這些屬性來判斷要用來完成傳輸要求的網路傳輸通訊協定和 SNMP 版本架構。 如需詳細資訊，請參閱 [關於 SNMP 版本](about-snmp-versions.md)。

-   實體和內容轉譯模式。

    此模式會使用此模式來解讀 SNMP 實體和內容的使用者易記名稱。 如需詳細資訊，請參閱 [設定實體和內容轉譯模式](setting-the-entity-and-context-translation-mode.md)。

-   重新傳輸原則設定。

    此執行會使用此設定來判斷是否應該執行應用程式的重新傳輸原則。 此實值會儲存每個目的地實體的超時值和重試計數。 如需詳細資訊，請參閱 [關於重新傳輸](about-retransmission.md) 和 [管理重新傳輸原則](managing-the-retransmission-policy.md)。

 

 




