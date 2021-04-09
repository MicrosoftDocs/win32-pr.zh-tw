---
description: Schannel 驗證程式需要認證;用戶端和伺服器都必須取得有效的認證，才能建立訊息交換的安全性內容。 如需示範此程式的範例，請參閱取得認證。
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: 取得 Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692932"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="2e077-104">取得 Schannel 認證</span><span class="sxs-lookup"><span data-stu-id="2e077-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="2e077-105">Schannel 驗證程式需要認證;用戶端和伺服器都必須取得有效的認證，才能建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="2e077-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="2e077-106">如需示範此程式的範例，請參閱 [取得認證](getting-a-certificate-for-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="2e077-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="2e077-107">您的應用程式會藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函式來取得認證，此函式會將控制碼傳回給要求的認證。</span><span class="sxs-lookup"><span data-stu-id="2e077-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="2e077-108">因為認證控制碼是用來儲存設定資訊，所以相同的控制碼無法同時用於用戶端和伺服器端作業。</span><span class="sxs-lookup"><span data-stu-id="2e077-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="2e077-109">這表示支援用戶端和伺服器連線的應用程式必須至少取得兩個認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="2e077-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="2e077-110">在 Windows XP 中，安全通道 [**認證結構會 \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) 指定下列各項：</span><span class="sxs-lookup"><span data-stu-id="2e077-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="2e077-111">安全性通訊協定</span><span class="sxs-lookup"><span data-stu-id="2e077-111">A security protocol</span></span>
-   <span data-ttu-id="2e077-112">允許的密碼</span><span class="sxs-lookup"><span data-stu-id="2e077-112">The allowable ciphers</span></span>
-   <span data-ttu-id="2e077-113">最小和最大加密強度</span><span class="sxs-lookup"><span data-stu-id="2e077-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="2e077-114">用於驗證的 [*x.509*](../secgloss/x-gly.md) 憑證—伺服器的必要參數，除非伺服器要求用戶端驗證，否則為用戶端選用。</span><span class="sxs-lookup"><span data-stu-id="2e077-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="2e077-115">透過 *pAuthData* 參數) [**，將安全通道認證結構 \_ (**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred)傳遞給 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函數。</span><span class="sxs-lookup"><span data-stu-id="2e077-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="2e077-116">此函數會傳回建立 [*安全性內容*](../secgloss/s-gly.md)所需的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="2e077-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="2e077-117">如需設定搭配 Schannel 使用之加密的詳細資訊，請參閱 [指定 Schannel 密碼和加密強度](specifying-schannel-ciphers-and-cipher-strengths.md)。</span><span class="sxs-lookup"><span data-stu-id="2e077-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="2e077-118">如需憑證的詳細資訊，請參閱 [憑證和憑證存放區功能](../seccrypto/cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="2e077-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="2e077-119">如需示範如何開啟 [*憑證存放區*](../secgloss/c-gly.md) 並尋找要用於 Schannel 驗證的憑證，請參閱 [取得憑證](getting-a-certificate-for-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="2e077-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
