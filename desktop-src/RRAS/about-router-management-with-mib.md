---
title: 關於使用 MIB 的路由器管理
description: 適用于路由器管理的管理資訊基礎 (MIB) Api，可讓您查詢和設定由其中一個路由器管理員或路由器管理員服務之任何路由通訊協定所匯出的 MIB 變數值。
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- 路由，管理資訊基礎
- 路由，管理資訊基礎，描述
- 管理資訊基礎 RRAS
- MIB
- MIB，請參閱管理資訊基礎
- 管理資訊基礎 RRAS
- 管理資訊基礎 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a867d903e0fb79f9360dc5f1cb485040ed4489b328365bc2daa063a35fbe27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792193"
---
# <a name="about-router-management-with-mib"></a>關於使用 MIB 的路由器管理

適用于路由器管理的管理資訊基礎 (MIB) Api，可讓您查詢和設定由其中一個路由器管理員或路由器管理員服務之任何路由通訊協定所匯出的 MIB 變數值。 藉由使用此 API，路由器可支援 (SNMP) 的簡易網路管理通訊協定。

在 SNMP 架構中，路由器中每個可管理的物件都會以具有唯一物件識別碼 (OID) 的變數來表示。 對應至每個 OID 的值，代表物件的目前狀態。 Oid 和值的集合稱為管理資訊基底 (MIB) 。 MprAdminMib 呼叫可讓開發人員透過其 OID 指定物件，並查詢或寫入 ( "Set" ) 物件的值。

若要查詢及設定 MIB 變數，服務呼叫的模組必須定義一組資料結構。 這些資料結構包括用來作為物件識別碼的結構，以及用來保存所要存取之 MIB 變數值的結構。 這些資料結構對除了 MIB 函式的呼叫者和服務呼叫的模組之外，都不是透明的。

服務 MIB 通話的模組是路由器管理員或其中一個路由通訊協定。 呼叫端必須指定路由器管理員，即使呼叫是由其中一個路由通訊協定處理。 在這種情況下，呼叫端應該指定對應至該路由通訊協定之通訊協定系列的路由器管理員。 例如，如果開放式最短路徑先 (OSPF) 路由通訊協定正在處理 MIB 呼叫，則呼叫端必須指定 IP 路由器管理員，因為 OSPF 屬於 IP 通訊協定系列。 在每個 MIB 函式中， *dwTransportId* 參數會指定路由器管理員，而 *RoutingPid* 參數會指定路由通訊協定。 路由器管理員也有獨特的 *RoutingPid*，因為某些 MIB 變數可能由路由器管理員本身處理。

您可以在不受管理的電腦上呼叫 MprAdminMib 函數。 查詢或寫入值的 MprAdminMIB 函式會以參數做為參數，以處理要管理的電腦。 使用 [**MprAdminMIBServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) 函式來建立與遠端電腦的連線，並取得此控制碼。 在呼叫所需的 MprAdminMIB 函式來完成特定的系統管理工作之後，請呼叫 [**MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) 函數來終止遠端電腦的連接。

[**MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate)和 [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset)函式會以 OID 和包含物件新值的緩衝區作為參數。

[**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget)、 [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst)和 [**MPRADMINMIBENTRYGETNEXT**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext)函式會以 OID 和指標變數的位址做為參數。 在成功傳回時，指標變數會指向包含物件值的緩衝區。 呼叫端應該藉由呼叫 [**MprAdminMIBBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) 函式釋放這個緩衝區的記憶體。

[**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst)和 [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext)函數可讓開發人員執行 *SNMP 逐步* 解說。 因為 Oid 經過排序，所以每個 OID，因此每個可管理的物件都有 *下* 一個 oid。 SNMP 逐步解說指的是藉由讀取或寫入一連串的 Oid 來往返 MIB 的某個部分。

所有的 MprAdminMib 呼叫會通過動態介面管理員 (維度) 。 根據 OID，DIM 會將呼叫傳遞給其中一個路由器管理員。  (IP 和 IPX 都支援 SNMP) 。 同樣地，根據 OID，路由器管理員可能會處理呼叫本身，或將呼叫傳遞給其中一個用戶端。 所有的路由器用戶端都必須執行和匯出下列函式，這些函式會對應至類似名稱的 MprAdminMIB 函式：

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




