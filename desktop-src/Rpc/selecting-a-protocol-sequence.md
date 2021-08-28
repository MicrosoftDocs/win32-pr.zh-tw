---
title: 選取通訊協定順序
description: 通訊協定序列是網路作業系統用來透過網路與其他電腦交談的語言。
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3470c303737f44e7e2d0aa52393fa893efa4634b4a2a4aa5c1bba47a832ae6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127748"
---
# <a name="selecting-a-protocol-sequence"></a>選取通訊協定順序

通訊協定序列是網路作業系統用來透過網路與其他電腦交談的語言。 更具體來說，RPC 應用程式必須指定代表 RPC 通訊協定、傳輸通訊協定和網路通訊協定組合的字串。

Microsoft RPC 支援三種 RPC 通訊協定：

-   網路運算架構連接導向的通訊協定 (NCACN) 
-   網路運算架構資料包協定 (NCADG) 
-   網路運算架構本機遠端程序呼叫 (NCALRPC) 

RPC 應用程式可以使用 NCALRPC 通訊協定來叫用在執行用戶端程式的同一部電腦上執行的伺服器程式所提供的程式。 目前這是在同一部電腦上，以不同的進程呼叫功能最有效率的方法。

您的應用程式所使用的傳輸和網路通訊協定，取決於網路支援的通訊協定。 現今許多網路（包括網際網路）都支援 TCP/IP。 其他常見的傳輸和網路通訊協定是 IPX/SPX、NetBIOS 和 AppleTalk DSP。 Microsoft RPC 支援這些和其他傳輸和網路通訊協定。 如需完整清單，請參閱 [通訊協定順序常數](protocol-sequence-constants.md)。

當您的應用程式使用自動系結控制碼時，不需要指定通訊協定順序。 如果它使用隱含或明確的控制碼，則必須取得或指定通訊協定順序。 每個分散式系統都必須檢查將部署的環境，以判斷哪一個通訊協定序列最適合該環境。

並非所有的通訊協定順序都有對等的功能。 開發人員應確認所選的通訊協定順序是否支援必要的功能。 一般情況下，建議使用 **ncalrpc** 進行本機通訊，並使用 **ncacn \_ ip \_ tcp** 或 **ncacn \_ HTTP** 進行遠端通訊; 它們可在所有環境中運作，且具有最佳效能，而且支援所有必要的最佳作法功能。

用戶端也可以指定它們從 Active Directory、登錄、安裝程式所建立及初始化的環境變數、應用程式特定的設定檔，或程式原始程式碼中的常值字串所取得的通訊協定順序資訊。

當您的用戶端程式具有有效的通訊協定順序字串之後，就可以將該資訊傳遞給 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 和 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 函式，以建立系結控制碼。

 

 




