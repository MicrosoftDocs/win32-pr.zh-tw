---
title: 設定實體和內容轉譯模式
description: 藉由設定實體和內容轉譯模式，WinSNMP 應用程式可以指定實體和內容參數的解讀和轉譯。 Microsoft WinSNMP 執行會將模式儲存在資料庫中。
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab459c0b33ffe1cc43c81858b57ec55942f61f2b5b736ca0124f31f52cc960d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009056"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>設定實體和內容轉譯模式

藉由設定實體和內容轉譯模式，WinSNMP 應用程式可以指定實體和內容參數的解讀和轉譯。 Microsoft WinSNMP 執行會將模式儲存在資料庫中。

實體和內容轉譯模式的設定會決定 [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) 函式和 [**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) 函數解讀輸入字串的方式。 這項設定也會決定 [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) 和 [**SnmpCoNtextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) 函數傳回的輸出字串類型。 如需詳細資訊，請參閱 [在 WinSNMP 中支援 IPX 位址字串](support-for-ipx-address-strings-in-winsnmp.md)。

在 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)函數的 *nTranslateMode* 參數中，此實值會傳回目前的預設實體和內容轉譯模式。 若要取得目前的實體和實際執行的內容轉譯模式，應用程式可以在任何時間呼叫 [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) 函數。

有效的實體和內容轉譯模式如下。

| [模式]                      | 意義                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ 轉譯       | 此執行會使用其資料庫來轉譯 SNMP 實體和 managed 物件的使用者易記名稱。 此執行會將它們轉譯成其 SNMPv1 或 SNMPv2C 元件。                                                                                                  |
| SNMPAPI 未 \_ 翻譯 \_ V1 | 此執行會將 SNMP 實體參數視為常值 snmp 傳輸位址，並將內容參數視為常值 SNMP 社區字串。 針對 SNMPv2 目的地實體，執行會在 [版本] 欄位中建立包含值為零的外寄 SNMP 訊息。 |
| SNMPAPI 未 \_ 翻譯 \_ V2 | 此執行會將 SNMP 實體參數解讀為 SNMP 傳輸位址，並將內容參數視為常值 SNMP 的社區字串。 針對 SNMPv2 目的地實體，執行會在 [版本] 欄位中建立包含值1的外寄 SNMP 訊息。            |



 

執行會嘗試將其資料庫中的資源與管理實體的常值傳輸位址產生關聯。

若要變更實體和內容轉譯模式，設定 WinSNMP 應用程式必須呼叫 [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) 函數。 如果要求的轉譯模式無效，函數會失敗，而 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 會傳回錯誤碼 SNMPAPI \_ 模式 \_ 無效。

 

 




