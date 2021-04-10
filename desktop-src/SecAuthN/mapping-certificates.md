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
# <a name="mapping-certificates"></a><span data-ttu-id="23fef-103">對應憑證</span><span class="sxs-lookup"><span data-stu-id="23fef-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="23fef-104">本主題中的資訊只適用于需要用戶端驗證的伺服器。</span><span class="sxs-lookup"><span data-stu-id="23fef-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="23fef-105">當伺服器應用程式要求用戶端驗證時，安全通道會自動嘗試將用戶端所提供的憑證對應至使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="23fef-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="23fef-106">建立 [*安全性內容*](../secgloss/s-gly.md)之後，伺服器應用程式可以使用 [**QuerySecurityCoNtextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken)函式來取得對應 [*用戶端憑證*](../secgloss/c-gly.md)之使用者帳戶的 [*存取權杖*](../secgloss/a-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="23fef-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="23fef-107">此外，伺服器也可以使用 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) 函數來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="23fef-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="23fef-108">如需有關驗證的詳細資訊，請參閱 [使用 Schannel 執行驗證](performing-authentication-using-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="23fef-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
