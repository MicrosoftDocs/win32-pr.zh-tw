---
title: 瞭解路由器管理功能
description: 下列各節將討論不同類型的路由器管理功能，以及有效使用這些功能的須知。
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85aac5cc2ec0167527f07c04459ec0aed7dbc248bed727fb4a949765c2fdcc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025398"
---
# <a name="understanding-router-management-functions"></a>瞭解路由器管理功能

下列各節將討論不同類型的路由器管理功能，以及有效使用這些功能的須知。

所有的路由器管理功能都需要系統管理員許可權。 Power User 群組中的使用者沒有足夠的許可權可以使用路由器管理功能。

## <a name="the-different-classes-of-router-management-functions"></a>不同類別的路由器管理功能

路由器管理功能可以分為管理功能和設定功能。 [管理](router-administration-functions.md)函式的前置詞為 MprAdmin，而設定[函數](router-configuration-functions.md)的前置詞為 MprConfig。 儘管有命名，也會使用這兩組函數來進行路由器管理。 MprAdmin 函式會直接在執行中的路由器上運作。 MprConfig 函式具有類似的功能，但會在登錄中儲存的路由器設定上運作。 這兩種類型的函數都會傳遞 [資訊區塊](router-information-functions.md)。

路由器管理函式也可以根據其所管理的路由器元件來分割：介面、路由器管理員或路由器管理員用戶端。

[路由器介面](router-interface-functions.md)函式的前置詞是 MprAdminInterface 或 MprConfigInterface。 使用這些函數來存取介面。 [路由器管理員](router-manager-transport-functions.md)函式的前置詞為 MprAdminTransport 或 MprConfigTransport。 使用這些功能來存取路由器管理員。 最後， [路由器管理員用戶端](router-manager-client-interfacetransport-functions.md) 函式的前置詞為 MprAdminInterfaceTransport 或 MprConfigInterfaceTransport。 使用這些功能來存取在路由器上執行的用戶端。

MprAdmin 函式的子集是 [MprAdminMib 函數](/windows/desktop/RRAS/about-router-management-with-mib)。 這些也會單獨操作執行中的路由。 不過，這些函式不會傳遞資訊區塊。 這些函式會為通訊協定設計工具提供額外的彈性，特別是用來抓取非設定資訊，例如統計資料。

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>確保變更會立即發生且持續存在

開發人員可以使用 [路由器設定功能](router-configuration-functions.md)直接變更路由器設定。 不過，在重新開機路由器之前，對設定所做的任何變更都不會生效，因為這是維度從登錄讀取設定的唯一時間。

開發人員可以使用 [路由器管理功能](router-administration-functions.md)來變更正在執行的路由器。 不過，這些變更不是持續性的：因為它們尚未寫入登錄中，所以如果重新開機路由器，就會遺失這些變更。

為了進行立即和持續性的變更，開發人員必須同時使用路由器管理與路由器設定功能。 如果路由器未執行，開發人員只需要呼叫適當的路由器設定功能。

若要從執行中的路由器查詢資訊，請使用路由器管理功能。 如果路由器未執行，請使用路由器設定函數來查詢資訊。

[**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)和 [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)函數支援 [**MPR \_ 介面 \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2)結構。 不過， [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) 和 [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) 則否。 若要建立在重新開機後持續的指定撥號介面，請使用 **MPR \_ interface \_ 2** 呼叫 **MprAdminInterfaceCreate** ，然後使用 [**MPR \_ interface \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)或 [**MPR \_ interface \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)呼叫 **MprConfigInterfaceCreate** 。 同樣地，若要對指定撥號介面進行持續變更，請使用 **MPR \_ interface \_ 2** 呼叫 **MprAdminInterfaceSetInfo** ，然後使用 **MPR \_ interface \_ 0** 或 **MPR \_ interface \_ 1** 呼叫 **MprConfigInterfaceSetInfo** 。

## <a name="using-router-administration-and-configuration-functions-remotely"></a>從遠端使用路由器管理和設定功能

大部分的路由器管理和設定功能都可以在不受管理的電腦上呼叫。 這些函式會採用作為參數、路由器服務的控制碼或要管理的設定。 管理函數會使用 RPC (遠端程序呼叫) 來與控制碼所指定的路由服務進行通訊。 設定函式會寫入至控制碼所指定之電腦的登錄，並從中讀取。

若要管理遠端電腦上的路由服務，請先呼叫 [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) 確認服務正在執行。 然後呼叫 [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) 來取得控制碼。 如果路由器服務未在遠端電腦上執行，則所有的路由器管理 (MprAdmin) 呼叫都將會失敗。

若要對遠端電腦上的路由器設定進行變更，請呼叫 [**MprConfigServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) 函式來取得控制碼。

 

 