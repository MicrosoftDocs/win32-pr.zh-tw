---
description: Microsoft Digest 需要使用者認證;用戶端和伺服器都必須顯示有效的認證，才能建立訊息交換的安全性內容。 認證控制碼可用來取得和出示認證。
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: 取得 Microsoft Digest 的 SSP 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468941"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="26088-104">取得 Microsoft Digest 的 SSP 認證</span><span class="sxs-lookup"><span data-stu-id="26088-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="26088-105">Microsoft Digest 需要使用者 [*認證*](../secgloss/c-gly.md) ;用戶端和伺服器都必須顯示有效的認證，才能建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="26088-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="26088-106">認證控制碼可用來取得和出示認證。</span><span class="sxs-lookup"><span data-stu-id="26088-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="26088-107">因為認證控制碼是用來儲存設定資訊，所以相同的控制碼無法同時用於用戶端和伺服器端作業。</span><span class="sxs-lookup"><span data-stu-id="26088-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="26088-108">這表示支援用戶端和伺服器連線的應用程式必須至少取得兩個認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="26088-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="26088-109">若要取得 Microsoft Digest 所需認證的控制碼，請呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函數。</span><span class="sxs-lookup"><span data-stu-id="26088-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="26088-110">下列 C 語言範例示範如何取得認證。</span><span class="sxs-lookup"><span data-stu-id="26088-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="26088-111">取得預設摘要認證</span><span class="sxs-lookup"><span data-stu-id="26088-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="26088-112">取得替代的摘要認證</span><span class="sxs-lookup"><span data-stu-id="26088-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 
