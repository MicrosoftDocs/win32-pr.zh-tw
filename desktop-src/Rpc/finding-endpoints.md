---
title: 尋找端點
description: 伺服器程式會接聽用戶端要求的端點。 端點字串的語法取決於您所使用的通訊協定順序。 例如，TCP/IP 的端點是埠號碼，具名管道的端點語法是有效的管道名稱。
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024a85704287db7e5f78bb67eee9b64a7c6dc84ce5724623450d36f743e5fa9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021278"
---
# <a name="finding-endpoints"></a>尋找端點

伺服器程式會接聽用戶端要求的端點。 端點字串的語法取決於您所使用的通訊協定順序。 例如，TCP/IP 的端點是埠號碼，具名管道的端點語法是有效的管道名稱。

端點有兩種類型：知名和動態。 您選擇的程式所使用的端點類型，會決定分散式應用程式或執行時間程式庫是否指定端點。

本節將討論端點，並提供如何尋找它們的資訊。 它會組織成下列主題：

-   [使用 Well-Known 端點](#using-well-known-endpoints)
-   [使用動態端點](#using-dynamic-endpoints)
-   [將 Well-Known 端點匯出至端點對應資料庫](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> *靜態端點* 和 *已知端點* 的條款是相等的，並且可交換使用。

 

您的用戶端應用程式可能會使用端點對應來判斷伺服器程式目前是否正在執行。 您的用戶端可以呼叫 [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids)、 [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)和 [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) ，以查看伺服器是否已在端點對應中註冊所需的特定介面。

## <a name="using-well-known-endpoints"></a>使用知名端點

已知的端點是伺服器程式每次執行時所使用的預先指派端點。 由於伺服器一律會接聽該特定端點，因此用戶端一律會嘗試連接到該端點。 知名的端點通常是由負責傳輸通訊協定的授權單位所指派。 因為伺服器主機電腦具有有限數量的可用端點，所以不建議應用程式開發人員使用已知的端點。 動態端點的另一個優點是它們可簡化系統的長期管理和維護。

分散式應用程式可以在字串中指定知名的端點，並將該字串作為參數傳遞至函式 [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)。 或者，端點字串也可以出現在 IDL 檔案介面標頭中，作為 \[ [端點](/windows/desktop/Midl/endpoint) \] 介面屬性的一部分。

您可以使用兩種方法來執行已知的端點：

-   在字串系結中指定所有資訊
-   在名稱服務資料庫中儲存已知的端點

開發應用程式時，您可以撰寫建立系結至分散式應用程式所需的所有資訊。 用戶端可以直接在字串中指定已知的端點，呼叫 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 來建立包含所有系結資訊的字串，並將此字串提供給函數 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) ，以取得控制碼。 用戶端和伺服器可以硬式編碼，以使用已知的端點，或寫入，讓端點資訊來自命令列、資料檔、設定檔案或 IDL 檔案。

您的用戶端應用程式也可以查詢名稱服務資料庫，以取得已知的端點資訊。

## <a name="using-dynamic-endpoints"></a>使用動態端點

特定伺服器的端點數目和特定的通訊協定順序通常會受到限制。 例如，當您使用 [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp) 通訊協定序列（指出 RPC 網路通訊使用 tcp/ip 進行通訊）時，只有有限的埠可用 (大部分的系統都只會開啟範圍1025到5000的) 。 RPC 執行時間程式庫可讓您視需要動態指派端點。 由於可能的介面 Uuid 數目幾乎沒有限制，因此使用介面 UUID 來指示呼叫會提供更多的空間來擴充和提供更大的彈性。

根據預設，當 RPC 執行時間程式庫函數查詢名稱服務資料庫時，會搜尋端點資訊。 如果端點是動態的，則名稱服務資料庫將不會包含端點資訊。 不過，查詢會將伺服器的名稱提供給您的用戶端程式。 然後，它可以搜尋伺服器的端點對應。

如果用戶端需要使用動態端點進行遠端程序呼叫，則慣用的方法是在部分綁定的系結控制碼上進行呼叫。 RPC 執行時間會以透明的方式解析端點。 這個方法優於使用 [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) 函式，因為它允許在 RPC 執行時間中使用 advanced 快取機制。

如果需要更明確地控制端點選取，用戶端可以呼叫 [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)、 [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)和 [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) 函式，一次搜尋一個專案的端點對應。

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>將知名端點匯出至端點對應資料庫

您可以混用兩種方法來尋找端點，尤其是當分散式系統從已知的端點模型轉換為動態端點模型時。 在這類轉換中，伺服器的中繼版本將使用已知的端點，但它也會向端點對應資料庫註冊已知的端點。 這種方法可讓使用已知端點的用戶端和使用動態端點的用戶端進行連接。 所有伺服器都升級之後，就可以部署只能使用動態端點的新用戶端版本。 所有用戶端都升級之後，最終的伺服器版本就可以停止使用已知的端點，而且只會開始使用動態端點。

這種方法可讓已開始使用已知端點的應用程式轉換路徑，但不需要同時更新所有伺服器和用戶端，即可遷移至動態端點。

 

 