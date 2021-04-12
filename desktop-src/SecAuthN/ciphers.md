---
description: 只有在使用 Digest 作為 SASL 機制時，下列材質才有效。 使用 Microsoft Digest 的 HTTP 驗證無法使用加密和加密。
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: 加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192103"
---
# <a name="ciphers"></a>加密

只有在使用 Digest 作為 SASL 機制時，下列材質才有效。 使用 Microsoft Digest 的 HTTP 驗證無法使用加密和加密。

摘要 SASL 挑戰的 cipher 指示詞包含伺服器所支援的密碼的清單，而伺服器需要機密通訊。 只有在 qop 指示詞設定為 "auth-會議" 時，才可以包含 cipher 指示詞。 下表列出由 Microsoft Digest 辨識的密碼，從最強到最弱的順序。



| 加密值 | Description                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| rc4        | 具有128位金鑰的 RC4 密碼。                                                                                                                                                                                                                                                             |
| 3des       | 在 [*CBC*](/windows/desktop/SecGloss/c-gly)模式中使用 EDE 的 [*三重 DES*](/windows/desktop/SecGloss/t-gly)加密，每個 E 階段都有相同的索引鍵 (兩個索引鍵模式) 。 金鑰總長度為112位。 |
| "rc4-56"     | 具有56位金鑰的 RC4 密碼。                                                                                                                                                                                                                                                              |
| "rc4-40"     | 具有40位金鑰的 RC4 密碼。                                                                                                                                                                                                                                                              |
| 演算法        | [*加密標準中的資料加密標準*](/windows/desktop/SecGloss/d-gly) (DES [*) 加密，*](/windows/desktop/SecGloss/c-gly) (CBC) 模式的56位金鑰。 |



 

當伺服器應用程式要求機密性時 (qop = "驗證人員" ) Microsoft Digest 將會產生一項挑戰，以提供用戶端安裝在伺服器上的所有加密，並支援摘要。 摘要用戶端會選取最強的可用加密。 如需指定機密性的詳細資訊，請參閱 [產生摘要挑戰](generating-the-digest-challenge.md)。

 

 
