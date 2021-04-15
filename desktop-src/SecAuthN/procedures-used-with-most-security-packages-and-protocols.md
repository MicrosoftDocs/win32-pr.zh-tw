---
description: 安全性支援提供者介面 (SSPI) 模型，會使用電腦或網路上可用的各種安全性封裝，為用戶端/伺服器傳輸應用程式提供單一介面。
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: 搭配大部分安全性封裝和通訊協定使用的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511229"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>搭配大部分安全性封裝和通訊協定使用的程式

[*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 模型，會使用電腦或網路上可用的各種 [*安全性封裝*](../secgloss/s-gly.md)，為用戶端/伺服器傳輸應用程式提供單一介面。 SSPI 允許應用程式使用安全性封裝，而不需要處理封裝的基礎 [*安全性通訊協定*](../secgloss/s-gly.md) 。 同時，SSPI 還允許複雜且安全感知的應用程式，利用特定安全性套件的先進功能。

應用程式會使用下列步驟來初始化 SSPI，以保護大部分安全性套件的網路連接：

-   [使用 SecBufferDesc 和之 secbuffer](using-secbufferdesc-and-secbuffer.md)
-   [初始化 SSPI](initializing-sspi.md)
-   [使用驗證建立安全連線](establishing-a-secure-connection-with-authentication.md)
-   [確保訊息交換期間的通訊完整性](ensuring-communication-integrity-during-message-exchange.md)
-   [結束 SSPI 會話](ending-an-sspi-session.md)

 

 
