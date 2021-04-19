---
title: 指定端點
description: 在遠端程序呼叫中指定已知和動態的端點， (RPC) 。
ms.assetid: fc39b527-11e6-45a7-b3b5-8bcf469633d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 373fb2818dd14670f5a939aa524c81fcdb05e20b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968297"
---
# <a name="specifying-endpoints"></a>指定端點

端點是遠端程序呼叫之伺服器進程的網路特定位址。 端點的實際名稱取決於所使用的通訊協定順序。 例如，TCP、UDP 和 HTTP 使用埠。 具名管道使用具名管道名稱。 用戶端/伺服器應用程式可以使用已知的端點或動態端點。 本節提供伺服器程式用來指定已知和動態端點的技巧。 下列主題將討論這項資訊：

-   [指定知名端點](#specifying-well-known-endpoints)
-   [指定動態端點](#specifying-dynamic-endpoints)

## <a name="specifying-well-known-endpoints"></a>指定知名端點

當您的伺服器使用已知的端點時，它可以在名稱服務資料庫專案中包含端點資料。 如果有，當用戶端從伺服器專案匯入系結控制碼時，用戶端的系結控制碼就會包含完整的伺服器位址，包括已知的端點。

您的伺服器程式也可以指定已知的端點，同時指定通訊協定順序。 叫用 [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) 或 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 函數。 兩者之間的差異在於，後者的函式有一個額外的參數，可讓您的伺服器用來控制動態埠配置。

如果您的伺服器程式以這種方式指定其端點資訊，它也應該呼叫 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) 函式，以在端點對應中註冊端點。 雖然端點一律是相同的，但用戶端可能會使用端點對應來尋找伺服器。

和通訊協定順序一樣，應用程式可以在其 IDL 檔案中指定端點資訊。 當它執行時，應叫用 [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) 或 [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) 函式，同時註冊通訊協定序列和端點。 在此情況下，用戶端可以透過 IDL 檔案中的介面規格來存取端點資訊。 因此，不需要呼叫 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) 函數。

## <a name="specifying-dynamic-endpoints"></a>指定動態端點

動態端點是伺服器主機電腦在伺服器開始執行時所指派的端點。 大部分的伺服器應用程式會使用動態端點，以避免在伺服器主機電腦系統上的可用埠數量有限時，與其他程式發生衝突。 不過，使用具名管道或 [**ncalrpc**](/windows/desktop/Midl/ncalrpc) 通訊協定序列的程式會有非常大的端點命名空間。 相較于使用其他傳輸的程式，其受益于動態端點。

伺服器程式會在端點對應資料庫中註冊動態端點。 如果您想要讓伺服器使用任何可用的端點，請呼叫 [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)、 [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)、 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 或 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)。 這會將 RPC 執行時間程式庫設定為使用動態端點)  (s 的所有或一個有效的通訊協定順序。 然後，伺服器應該呼叫 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 來取得一組有效的系結控制碼。 伺服器會將一組系結控制碼或系結向量傳遞至函式 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) ，以註冊端點對應中所有適合的端點。 針對您的伺服器對 **RpcEpRegister** 進行的每個呼叫，應該會有對應的 [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) 呼叫，以釋放系結向量所使用的記憶體。

請注意，伺服器程式可以使用 [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) 函數，而不是 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)。 當伺服器程式的多個複本必須在伺服器主機系統上執行時，程式通常會使用 **RpcEpRegisterNoReplace** 。

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)和 [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace)函數都會將伺服器的介面和系結控制碼新增至端點對應程式資料庫。 當用戶端使用部分系結的控制碼進行遠端程序呼叫時，用戶端的執行時間程式庫會向伺服器電腦的端點對應程式要求相容伺服器實例的端點對應程式。 用戶端程式庫會在用戶端系結控制碼中提供介面 UUID、通訊協定順序，以及（如果有的話）物件 UUID。 端點對應程式會尋找符合用戶端資訊的資料庫專案。 用戶端/伺服器介面 UUID、介面主要版本和通訊協定順序都必須完全相符。 此外，伺服器的介面次要版本必須大於或等於用戶端的次要版本。

如果所有測試都成功，則端點對應程式會傳回有效的端點，而用戶端執行時間程式庫會更新系結控制碼中的端點。

當伺服器進程停止執行時，系統會自動從端點對應程式資料庫清除動態端點。 您可以先從端點對應程式資料庫移除端點，然後再使用 [**RpcEpUnregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepunregister) 函式結束伺服器程式，或者您可以允許自動清除來管理端點的移除作業。

 

 