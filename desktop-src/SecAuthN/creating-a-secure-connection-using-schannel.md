---
description: 如何使用 Schannel 建立安全的連接。
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: 使用 Schannel 建立安全連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374955b67bfa0026da5e8f8e9e88ce71da24231e218cb869cb532d05d4171bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008906"
---
# <a name="creating-a-secure-connection-using-schannel"></a>使用 Schannel 建立安全連線

Schannel [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 可讓您存取四種 [*安全性通訊協定*](/windows/desktop/SecGloss/s-gly)：

-   [傳輸層安全性 (TLS 1.2) ](transport-layer-security-protocol.md)
-   [傳輸層安全性 (TLS 1.1) ](transport-layer-security-protocol.md)
-   [傳輸層安全性 (TLS 1.0) ](transport-layer-security-protocol.md)
-   [安全通訊端層 (SSL 3.0) ](secure-sockets-layer-protocol.md)
-   [安全通訊端層 (SSL 2.0) ](secure-sockets-layer-protocol.md)

> [!Note]  
> PCT 和 SSL 2.0 通訊協定已被 TLS 通訊協定取代，且不應該用於新的開發。

 

**設定用戶端與伺服器之間的安全連線**

1.  取得安全通道認證 (取得) 的 [Schannel 認證](obtaining-schannel-credentials.md) 。
2.  建立 Schannel 安全性內容 ([建立安全通道安全性內容](creating-an-schannel-security-context.md)) 。

建立連線之後，您可以取得其屬性的相關資訊。 如需詳細資訊，請參閱 [取得 Schannel 連接的相關資訊](getting-information-about-schannel-connections.md)。

如果您在建立連線之後，應用程式的安全性需求變更或連接已遺失，您就可以重新協商連接。 如需詳細資訊，請參閱 [重新交涉 Schannel 連接](renegotiating-an-schannel-connection.md)。

當您完成使用 Schannel 連接時，必須執行必要的清除。 如需詳細資訊，請參閱 [關閉 Schannel 連接](shutting-down-an-schannel-connection.md)。

如需平臺軟體發展工具組隨附的範例 (SDK) （示範 Schannel [*安全性封裝*](/windows/desktop/SecGloss/s-gly)）的相關資訊，請參閱使用 SCHANNEL 的 PSDK 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定 Schannel 密碼和加密的強度](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
