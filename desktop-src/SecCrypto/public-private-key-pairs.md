---
description: 非對稱金鑰也稱為公開/私密金鑰組，用於非對稱式加密。 非對稱式加密主要是用來加密和解密工作階段金鑰和數位簽章。 非對稱式加密會使用公開金鑰加密演算法。
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: 非對稱金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374ba5ae17610154e306f7bdafd895116e83371ea446babfa19b5c92c29a2247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901470"
---
# <a name="asymmetric-keys"></a>非對稱金鑰

[*非對稱金鑰*](../secgloss/a-gly.md)也稱為 [*公開/私密金鑰*](../secgloss/p-gly.md)組，用於非對稱式加密。 非對稱式加密主要是用來加密和解密 [*工作階段金鑰*](../secgloss/s-gly.md) 和 [*數位簽章*](../secgloss/d-gly.md)。 非對稱式加密會使用 [*公開金鑰加密*](../secgloss/p-gly.md) 演算法。

公開金鑰演算法使用兩個不同的索引鍵： [*公開金鑰*](../secgloss/p-gly.md) 和 [*私密金鑰*](../secgloss/p-gly.md)。 配對的私密金鑰成員必須保持私用且安全。 不過，公開金鑰可以散發給要求的任何人。 金鑰組的公開金鑰通常是透過 [*數位憑證*](../secgloss/c-gly.md)來散發。 使用金鑰組的其中一個金鑰來加密訊息時，需要該配對的另一個金鑰才能解密訊息。 因此，如果使用使用者 A 的公開金鑰來加密資料，則只有使用者 A (或有權存取使用者 A 私密金鑰) 的人員可以解密資料。 如果使用使用者 A 的私密金鑰來加密某一段資料，則只有使用者 A 的公開金鑰會解密資料，藉此表示使用者 A (或存取使用者 A 私密金鑰的人員) 進行加密。

如果使用私密金鑰來簽署訊息，則必須使用該配對的公開金鑰來驗證簽章。 例如，如果 Alice 想要將數位簽署的訊息傳送給某人，她會使用她的私密金鑰來簽署訊息，而另一個人可以使用她的公開金鑰來驗證她的簽章。 由於只有 Alice 可以存取她的私密金鑰，因此可以使用 Alice 的公開金鑰來驗證簽章，這表示 Alice 已建立簽章。

可惜的是，公開金鑰演算法的速度很慢，大約1000倍于對稱演算法。 使用它們來加密大量資料是不切實際的。 在實務上，公開金鑰演算法會用來加密 [*工作階段金鑰*](../secgloss/s-gly.md)。 [*對稱演算法*](../secgloss/s-gly.md) 用來加密/解密大部分的資料。

同樣地，因為簽署訊息實際上會加密訊息，所以使用公開金鑰簽章演算法來簽署大型訊息並不實用。 相反地，訊息會產生固定長度的 [*雜湊*](../secgloss/h-gly.md) ，並簽署雜湊值。 如需詳細資訊，請參閱 [雜湊和數位簽章](hashes-and-digital-signatures.md)。

每個使用者一般都有兩組 [*公開/私密金鑰*](../secgloss/p-gly.md)組。 一個金鑰組可用來加密工作階段金鑰，另一個則用來建立 [*數位簽章*](../secgloss/d-gly.md)。 分別稱為「 [*金鑰交換金鑰*](../secgloss/k-gly.md) 組」和「簽章 [*金鑰*](../secgloss/s-gly.md)組」。

請注意，雖然大多數 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 所建立的金鑰容器 (csp) 包含兩個金鑰組，但這並不是必要的。 有些 Csp 不會儲存任何 [*金鑰*](../secgloss/k-gly.md) 組，其他 csp 則儲存兩組以上。

CryptoAPI 中的所有金鑰都儲存在 Csp 內。 Csp 也負責建立金鑰、終結它們，以及使用它們來執行各種不同的密碼編譯作業。 從 CSP 匯出金鑰，以便將金鑰傳送給其他使用者，[儲存體和 Exchange 的密碼編譯金鑰](cryptographic-key-storage-and-exchange.md)中有討論。

 

 
