---
description: 對應憑證
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: 對應憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694147"
---
# <a name="mapping-certificates"></a>對應憑證

> [!Note]  
> 本主題中的資訊只適用于需要用戶端驗證的伺服器。

 

當伺服器應用程式要求用戶端驗證時，安全通道會自動嘗試將用戶端所提供的憑證對應至使用者帳戶。

建立 [*安全性內容*](../secgloss/s-gly.md)之後，伺服器應用程式可以使用 [**QuerySecurityCoNtextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken)函式來取得對應 [*用戶端憑證*](../secgloss/c-gly.md)之使用者帳戶的 [*存取權杖*](../secgloss/a-gly.md)。 此外，伺服器也可以使用 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) 函數來模擬用戶端。

如需有關驗證的詳細資訊，請參閱 [使用 Schannel 執行驗證](performing-authentication-using-schannel.md)。

 

 
