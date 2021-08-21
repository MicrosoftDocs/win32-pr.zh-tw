---
description: 憑證是根據定義要求者必須符合以接收憑證之準則的原則來授與。
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: 原則獨立性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63afc249905dc03602e38458ba326674e033648669e3187d44e58a188b122d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978964"
---
# <a name="policy-independence"></a>原則獨立性

憑證是根據定義要求者必須符合以接收憑證之準則的原則來授與。 例如，一個原則可能是只有在申請人出示其身分識別時，才授與商業憑證。 另一個原則可能會根據電子郵件要求授與 [*認證*](../secgloss/c-gly.md) 。 發出信用卡的機構可以選擇查閱資料庫，並在發出卡片之前進行電話查詢。

原則會在以 c + +、C 或 Visual Basic 撰寫的原則模組中執行。 憑證服務函式與機構可能會實行的原則中的任何變更隔離。 原則中的變更可以完整地在伺服器原則模組程式碼中執行。  (CA) 的企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位只能使用 Microsoft 提供的企業原則模組。

 

 
