---
description: Kerberos 通訊協定會定義用戶端如何與網路驗證服務 \[ 平臺軟體發展工具組 (SDK) 互動 \] 。
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos (英文)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680a55581394d9d36da5b54cb2365d07384893069e26f9787163209daf2eabd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921790"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos (英文)

[*Kerberos 通訊協定*](../secgloss/k-gly.md)會定義用戶端與網路驗證服務的互動方式。 用戶端從 Kerberos 金鑰發佈中心 (KDC) 取得票證，並在建立連線時將這些票證呈交給伺服器。 Kerberos 票證代表用戶端的網路 [*認證*](../secgloss/c-gly.md)。

本節中的資訊提供在驗證程式中使用 Kerberos 通訊協定的理論背景。 這是可讓開發人員瞭解在使用 Kerberos 第5版通訊協定的 SSPI 進程中幕後發生什麼事的背景資訊。

Kerberos 驗證通訊協定會在建立安全的網路連接之前，提供實體之間的相互驗證機制。 在這整份檔中，這兩個實體稱為用戶端和伺服器，即使可以在伺服器之間建立安全的網路連接也是一樣。 用戶端和伺服器也可以稱為 [*安全性主體*](../secgloss/s-gly.md)。

Kerberos 通訊協定會假設用戶端和伺服器之間的交易會在開啟的網路上進行，其中大部分的用戶端和許多伺服器並不安全，而且透過網路移動的封包也可以進行監視和修改。 假設的環境就像是現今的網際網路，攻擊者可以輕鬆地將它視為用戶端或伺服器，而且可以輕易竊聽或篡改合法用戶端與伺服器之間的通訊。

本節提供下列資訊：

-   [基本驗證概念](basic-authentication-concepts.md)
-   [Kerberos Subprotocols](kerberos-subprotocols.md)
-   [Kerberos 模型](kerberos-components.md)
-   [SSPI/Kerberos 與 GSSAPI 的互通性](sspi-kerberos-interoperability-with-gssapi.md)

您的應用程式不應直接存取 Kerberos [*安全性套件*](../secgloss/s-gly.md) ;相反地，它應該使用 [*Negotiate*](../secgloss/n-gly.md) 安全性封裝。 Negotiate 可讓您的應用程式利用更高階的 [*安全性通訊協定*](../secgloss/s-gly.md) （如果驗證所含的系統支援的話）。 目前，協商安全性封裝會在 [*Kerberos*](../secgloss/k-gly.md) 和 NTLM 之間進行選取。 除非其中一個與驗證相關的系統無法使用，否則 Negotiate 會選取 Kerberos。

 

 
