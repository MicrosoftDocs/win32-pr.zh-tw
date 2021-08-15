---
description: 分散式應用程式的 SSPI 選項
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: 分散式應用程式的 SSPI 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfeef5cb52494c50b8b16911f70de238a7a86493297ec59bf6d46637810bf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916788"
---
# <a name="sspi-options-for-distributed-applications"></a>分散式應用程式的 SSPI 選項

開發人員有許多選項可建立分散式應用程式。 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 在應用層級通訊協定和 [*安全性通訊協定*](../secgloss/s-gly.md)之間提供抽象層。 應用程式可以透過數種方式來利用 SSPI 安全性通訊協定：

-   針對傳統的通訊端型應用程式) 直接呼叫 SSPI 常式 (。

    常式會使用要求/回應訊息來執行 [*應用程式協定，此通訊協定*](../secgloss/a-gly.md) 會攜帶 SSPI 安全性相關資料。

-   使用 COM 來呼叫在較低層級使用已驗證的 RPC 和 SSPI 所執行的安全性選項。

    這些應用程式不會直接呼叫 SSPI 函數。

-   使用[Windows 通訊端 2](../winsock/windows-sockets-start-page-2.md) (WinSock) 搭配擴充的 WinSock 介面，以允許傳輸提供者使用安全性功能。

    這種方法會將 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 整合到網路堆疊中，並透過通用介面提供安全性與傳輸服務。

-   使用 [Windows 的網際網路擴充 API](../wininet/portal.md) (WinInet) 以及設計來支援網際網路安全性通訊協定（例如 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定）的介面。

    應用程式會將 SSPI 介面用於 [安全通道](secure-channel.md) (Schannel) 安全性提供者來實行 WinInet 安全性。 Schannel 是 Microsoft 的 SSL 執行。

數個 SSPI 函式會傳回代表各種物件存留期的時間戳記。 [*安全性套件*](../secgloss/s-gly.md) 可以維持時間，並以不同的方式提供時間戳記，但使用本地時間可簡化使用 SSPI 函式的應用程式工作。

 

 
