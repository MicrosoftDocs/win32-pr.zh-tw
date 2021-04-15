---
description: 主要金鑰是衍生其他金鑰的主要資料材質。
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: 建立主要金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511175"
---
# <a name="creating-the-master-key"></a>建立主要金鑰

[*主要金鑰*](../secgloss/m-gly.md)是衍生其他金鑰的主要資料材質。 根據所使用的通訊協定和加密套件，主要金鑰的長度可以是5到48個位元組。 針對 [*rsa*](../secgloss/r-gly.md)安全通道 / [](../secgloss/s-gly.md) CSP，主要金鑰是由用戶端所建立，並傳輸至 RSA 信封中的伺服器。 若是 [*Diffie-hellman*](../secgloss/d-gly.md)/Schannel CSP，主要金鑰是藉由執行 Diffie-Hellman 金鑰交換來建立。

以下示範建立和交換主要金鑰的程式碼：

-   [用來建立主要金鑰的 diffie-hellman 用戶端程式代碼](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [建立主要金鑰的 diffie-hellman 伺服器程式碼](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [用來建立主要金鑰的 RSA 用戶端程式代碼](rsa-client-code-for-creating-the-master-key.md)
-   [用來建立主要金鑰的 RSA 伺服器程式碼](rsa-server-code-for-creating-the-master-key.md)
-   [指定演算法](specifying-the-algorithms.md)

 

 
