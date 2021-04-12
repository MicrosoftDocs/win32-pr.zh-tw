---
description: 密碼編譯金鑰是密碼編譯作業的核心。
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: 密碼編譯金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82858b26fa70ceacb4e7f9714e29983a773e66ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468896"
---
# <a name="cryptographic-keys"></a>密碼編譯金鑰

[*密碼編譯金鑰*](../secgloss/c-gly.md) 是密碼編譯作業的核心。 許多密碼編譯配置都包含一組作業，例如加密和解密，或是簽署和驗證。 索引 *鍵* 是一段變數資料，會作為輸入送入密碼編譯演算法，以執行這類作業。 在設計完善的密碼編譯配置中，配置的安全性只取決於所使用的金鑰安全性。

密碼編譯金鑰可根據其在密碼編譯配置中的使用方式進行分類，作為 [對稱金鑰](symmetric-keys.md) 或 [非對稱金鑰](public-private-key-pairs.md)。 [*對稱金鑰*](../secgloss/s-gly.md)是在密碼編譯配置中用來進行這兩項作業的單一金鑰 (例如，[*加密*](../secgloss/e-gly.md)和 [*解密*](../secgloss/d-gly.md)您的資料) 。 通常，配置的安全性取決於確保只有授權的參與者知道金鑰。 另一方面，非對稱金鑰用於每個作業都需要不同金鑰的密碼編譯配置。 這類架構的常見範例是使用 [*公開/私密金鑰*](../secgloss/p-gly.md)組的範例，其中配置的安全性取決於確保只有一個合作物件知道 [*私密金鑰*](../secgloss/p-gly.md) 。 例如，公開/私密金鑰加密系統使用兩個金鑰，也就是任何人都能用來加密資料的 [*公開金鑰*](../secgloss/p-gly.md) ，以及一個只是授權的收件者所擁有，而且可以用來解密資料的 [*私*](../secgloss/p-gly.md) 用金鑰。

密碼編譯金鑰可依使用的用途進一步分類。 這些用途包括數位簽章產生、數位簽章驗證、訊息驗證、資料加密和解密、金鑰包裝和金鑰傳輸。 如需完整的金鑰類型清單（如美國國家標準 [*和技術局*](../secgloss/n-gly.md) (NIST) 所定義），請參閱 Nist 特殊發行800-57 的一般金鑰管理指導方針 [-第1部分：一般 (修訂)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf)。

 

 
