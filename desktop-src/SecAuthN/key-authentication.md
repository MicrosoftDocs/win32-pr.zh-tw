---
description: 許多形式的驗證都是以實體可證明其身分識別的概念為基礎，如果它可以證明它知道只有它知道的金鑰（例如密碼）。
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: 金鑰驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193084"
---
# <a name="key-authentication"></a>金鑰驗證

許多形式的驗證都是以實體可證明其身分識別的概念為基礎，如果它可以證明它知道只有它知道的金鑰（例如密碼）。

依賴秘密的驗證技術（例如密碼）必須要有一種方法來防止秘密成為公開知識。 密碼擁有者無法向上移至大門並提供密碼。 Doorkeeper 以外的人可能正在接聽;或者它可能是錯誤的門。 為了保留秘密，必須有方法證明使用者知道密碼，而不會洩漏密碼。 這是秘密金鑰驗證背後的概念，也就是在 [*Kerberos 通訊協定*](../secgloss/k-gly.md)中使用的一種驗證方法。

請注意，秘密金鑰驗證中的「秘密」是指驗證程式是在「秘密」中進行，亦即，實際上不會洩漏金鑰的內容。

若要讓秘密金鑰驗證正常運作，交易的雙方必須共用密碼編譯 [*工作階段金鑰*](../secgloss/s-gly.md) ，也就是秘密，而且沒有人知道。 金鑰為 [*對稱*](../secgloss/s-gly.md)式;也就是說，它是用於加密和解密的單一金鑰。 驗證程式中的一方會藉由加密訊息來證明其金鑰的知識。 另一方藉由解密訊息來證明其金鑰的知識。

 

 
