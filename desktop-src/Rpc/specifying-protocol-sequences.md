---
title: 指定通訊協定順序
description: 伺服器應用程式必須選取一或多個通訊協定順序，以在透過網路與用戶端進行通訊時使用。 通訊協定順序的選擇與網路相依。 請參閱解讀系結資訊和選取通訊協定順序。
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f43b8dc7b21fc2a6bebe98010b80dbf369ac96bb185cc75afa3b0a4f1acbba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925148"
---
# <a name="specifying-protocol-sequences"></a>指定通訊協定順序

伺服器應用程式必須選取一或多個通訊協定順序，以在透過網路與用戶端進行通訊時使用。 通訊協定順序的選擇與網路相依。 請參閱解讀系結 [資訊](interpreting-binding-information.md) 和 [選取通訊協定順序](selecting-a-protocol-sequence.md)。

您的伺服器程式可能會允許用戶端使用網路支援的任何通訊協定順序來進行連接。 若要這樣做，請叫用 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) 並傳遞 RPC \_ C \_ PROTSEQ \_ MAX \_ 先決條件 \_ DEFAULT 作為第一個參數。 不過，這不是建議的方法。 相反地，針對遠端呼叫使用 **ncalrpc** 進行本機呼叫和 **ncacn \_ ip \_ tcp** 或 **ncacn \_ HTTP** 通常就已足夠。 [不尋常的網路] 很罕見，而且幾乎所有網路都支援 TCP/IP。

如果您想要讓用戶端將動態端點的埠配置限制為特定的埠範圍，請改為呼叫 [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) 。 這是 Microsoft RPC 專用的函式，對於通過防火牆的遠端程序呼叫而言非常有用。 它會使用額外的參數將埠配置控制旗標傳遞給函式。 請參閱設定登錄 [的埠配置和選擇性](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md)系結。

您可以在開發伺服器的介面時，于 MIDL 檔案中指定通訊協定序列和端點資訊。 如果您這樣做，您的伺服器應該使用 [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) 來註冊 IDL 檔案中提供的所有通訊協定序列和相關聯的端點資訊。 此外，也有一個對應的 [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) 函式，也可讓伺服器傳遞通訊埠配置（控制旗標）。

如果您想要將用戶端和伺服器程式設定為與指定的通訊協定順序通訊，伺服器應用程式應該呼叫 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)。 如需 Microsoft RPC 通訊協定順序的完整清單，請參閱 [通訊協定順序常數](protocol-sequence-constants.md)。

Microsoft RPC 也提供 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) ，讓應用程式可以選取特定的通訊協定順序，以及控制動態埠配置。

除了連接導向的通訊協定以外，Microsoft RPC 也支援資料包 (無連線的) 通訊協定。 建議使用連線導向的通訊協定;資料包通訊協定與連接導向的通訊協定具有不同的功能集，只有在分散式系統開發人員需要的功能只適用于資料包通訊協定時，才會使用。 使用資料包通訊協定時可用的部分功能包括：

-   資料包支援 UDP 和 IPX 無連接傳輸通訊協定。
-   因為不需要建立和維護連線，所以資料包 RPC 通訊協定需要較少的資源負擔。
-   資料包可加快系結的速度。
-   如同連接導向 RPC，資料包 RPC 呼叫預設為 *nonidempotent*。 這表示不保證會執行一次以上的呼叫。 不過，函式可以在 IDL 檔案中標示為等冪，告知 RPC 在回應單一用戶端要求時，不會多次執行函數。 這可讓執行時間在伺服器上維持較少的狀態。 請注意，等冪呼叫只會在不穩定網路上的罕見情況下重新執行。
-   資料包 RPC 支援 [廣播](/windows/desktop/Midl/broadcast) IDL 屬性。 廣播可讓用戶端同時對多部伺服器發出訊息。 這可讓用戶端找到網路上數個可用伺服器的其中一個，或同時控制多部伺服器。 請注意，資料包廣播只在本機連結內有效，且通常不會跨路由器。 廣播呼叫是隱含等冪的。 如果呼叫包含 \[ **out** \] 參數，則只會傳回第一個伺服器回應。 一旦伺服器回應，所有未來對該系結控制碼的 Rpc 都只會傳送到該伺服器，包括具有廣播屬性的呼叫。 若要傳送另一個廣播，請建立新的系結控制碼，或在現有的控制碼上呼叫 [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) 。
-   資料包 RPC 支援 [可能](/windows/desktop/Midl/maybe) 的 IDL 屬性。 這可讓用戶端傳送呼叫給伺服器，而不需等待回應或確認。 呼叫不能包含 \[ **out** \] 參數。 使用的呼叫 **\[ 可能 \]** 會隱含等冪。

 

 