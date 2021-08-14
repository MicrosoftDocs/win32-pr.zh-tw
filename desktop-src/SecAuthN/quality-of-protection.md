---
description: Qop 指示詞所識別的保護品質是由伺服器在摘要式挑戰中指定，然後由用戶端在挑戰回應中確認。
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: 保護品質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202acbf319601af74efc35117990f27cc6edff76f27da243453f82bf50984977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920447"
---
# <a name="quality-of-protection"></a>保護品質

Qop 指示詞所識別的保護品質是由伺服器在摘要式挑戰中指定，然後由用戶端在挑戰回應中確認。 如果用戶端需要伺服器不支援的保護品質，用戶端必須終止驗證。

下表說明 qop 指示詞的可能值。



| 值                   | 描述                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 作者                  | 僅限於驗證 (Authentication)。                                                                                                                         |
| "auth-int"              | 使用簽章進行驗證和 [*完整性*](../secgloss/i-gly.md) 檢查。                  |
|  (SASL 僅) 「驗證」 | 使用簽章和加密進行驗證、完整性和機密性檢查。 如需詳細資訊，請參閱 [密碼](ciphers.md)。 |



 

保護品質取決於傳遞給 Microsoft Digest SSP 的內容需求旗標。 下表列出與保護品質相關的旗標，以及 qop 指示詞的結果值。



| 旗標                         | qop 值               |
|------------------------------|-------------------------|
| *XXX* \_要求 \_ 機密性  | 「驗證」 (SASL 僅)  |
| *XXX* \_要求重新執行偵測 \_ \_   | "auth-int"              |
| *XXX* \_要求 \_ 順序 \_ 偵測 | "auth-int"              |
| *XXX* \_需求 \_ 完整性        | "auth-int"              |
| (無)                       | 作者                  |



 

> [!Note]  
> 伺服器應用程式所指定的內容需求旗標具有 ASC 的前置詞，而用戶端指定的旗標則以 ISC 作為前置詞。 若要判斷您的應用程式所使用的旗標值，請將這些首碼中的其中一個設為 *XXX*。

 

如需其他伺服器相關資訊，請參閱 [產生摘要挑戰](generating-the-digest-challenge.md)。

如需其他用戶端的相關資訊，請參閱 [產生摘要挑戰回應](generating-the-digest-challenge-response.md)。

 

 
