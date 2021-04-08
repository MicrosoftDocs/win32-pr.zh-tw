---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671035"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Microsoft RPC 是在分散式運算環境中進行程式設計的模型。 RPC 的目標是要提供透明通訊，讓用戶端看起來與伺服器直接通訊。 Microsoft 的 RPC 執行與開放式 Software Foundation (憑證) 分散式運算環境 (DCE) RPC 相容。

您可以設定 RPC 使用一或多個傳輸、一或多個名稱服務，以及一或多個安全性伺服器。 這些提供者的介面是由 RPC 處理。 由於 Microsoft RPC 是設計來與多個提供者搭配使用，因此您可以選擇最適合您網路的提供者。 傳輸會負責在網路上傳輸資料。 名稱服務會接受物件名稱（例如，標記），並在網路上尋找其位置。 安全性伺服器提供應用程式拒絕存取特定使用者及/或群組的選項。 如需應用程式安全性的詳細資訊，請參閱 [介面設計規則](interface-design-rules.md) 。

除了 RPC 執行時間程式庫，Microsoft RPC 還包含介面定義語言 (IDL) 及其編譯器。 雖然 IDL 檔案是 RPC 的標準元件，但 Microsoft 已增強它以擴充其功能，以支援自訂 COM 介面。 Microsoft 介面定義語言 (MIDL) 編譯器使用 IDL 檔案來描述您的自訂介面，以產生 [建立和註冊 PROXY DLL](building-and-registering-a-proxy-dll.md)中所討論的數個檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[通道](channel.md)
</dt> <dt>

[物件間通訊](inter-object-communication.md)
</dt> <dt>

[封送處理詳細資料](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[存根](stub.md)
</dt> </dl>

 

 




