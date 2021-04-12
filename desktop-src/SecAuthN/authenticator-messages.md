---
description: 在使用秘密金鑰驗證的簡單通訊協定中，用戶端會以工作階段金鑰中加密資訊的形式呈現驗證者訊息。
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: 驗證器訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e76cf171d163ac2f1d0d4a7fcaab53a7fa0ace0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193284"
---
# <a name="authenticator-messages"></a>驗證器訊息

在使用秘密金鑰驗證的簡單通訊協定中，用戶端會以 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)中加密資訊的形式呈現驗證者訊息。 驗證通訊協定每次執行時，驗證器訊息中的資訊必須不同，或未經授權的實體可以重複使用加密的驗證器訊息。

當接收驗證器訊息時，伺服器會將它解密，並可從解密訊息的內容中得知解密是否成功。 如果解密的訊息不是很雜亂，伺服器會知道呈現驗證器訊息的用戶端使用正確的金鑰來加密訊息。 只有兩個實體可存取 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly) ，如果伺服器是這些實體，則加密驗證器訊息的用戶端必須是另一個。

若為相互驗證，則會執行類似的通訊協定。 伺服器會從解密的原始驗證器訊息中解壓縮部分資訊，使用共用工作階段金鑰加密它，然後將加密的訊息傳送給用戶端。 用戶端會解密訊息，並將結果與原始的結果進行比較。 如果解密的訊息符合原始訊息的正確部分，則用戶端知道伺服器可以使用共用密碼工作階段金鑰來解密原始訊息，而且可以使用相同的共用密碼 [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)重新加密該訊息的一部分。

 

 
