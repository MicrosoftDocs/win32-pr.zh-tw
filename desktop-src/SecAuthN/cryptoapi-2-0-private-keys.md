---
description: Schannel 認證會在內部表示為憑證 \_ 內容結構。
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 私密金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984556"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="986e2-103">CryptoAPI 2.0 私密金鑰</span><span class="sxs-lookup"><span data-stu-id="986e2-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="986e2-104">Schannel 認證會在內部表示為憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 結構。</span><span class="sxs-lookup"><span data-stu-id="986e2-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="986e2-105">Schannel 會使用[](/windows/desktop/SecGloss/p-gly)憑證的 CERT \_ key \_ >prov \_ INFO \_ \_ ID 屬性，找出與特定憑證內容相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="986e2-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="986e2-106">使用這個屬性，Schannel 會藉由呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta)函式來存取 *私密金鑰*。</span><span class="sxs-lookup"><span data-stu-id="986e2-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="986e2-107">如需其他詳細資訊，請參閱 [公開/私密金鑰](/windows/desktop/SecCrypto/public-private-key-pairs)組。</span><span class="sxs-lookup"><span data-stu-id="986e2-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="986e2-108">每個 Schannel 認證都包含一或多個私密金鑰的參考，每個私密金鑰都與特定憑證相關聯。</span><span class="sxs-lookup"><span data-stu-id="986e2-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="986e2-109">[*私密金鑰*](/windows/desktop/SecGloss/p-gly)的處理方式會有很大的不同，這取決於用戶端或伺服器的認證是否正確。</span><span class="sxs-lookup"><span data-stu-id="986e2-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="986e2-110">用戶端私密金鑰</span><span class="sxs-lookup"><span data-stu-id="986e2-110">Client Private Keys</span></span>

<span data-ttu-id="986e2-111">用戶端 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 是由 (CSP) 使用中的 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) 所管理。</span><span class="sxs-lookup"><span data-stu-id="986e2-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="986e2-112">用戶端私密金鑰通常會由 [>prov \_ rsa \_ FULL](/windows/desktop/SecCrypto/prov-rsa-full) 或 >prov rsa 簽章類型的 csp 儲存 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="986e2-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="986e2-113">如果用戶端應用程式在呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)之前以手動方式進行 [**CryptAcquireCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta)呼叫，用戶端必須使用 CERT \_ KEY \_ >prov \_ 控制碼 \_ \_ 識別碼屬性，將 CSP 的控制碼系結至憑證內容。</span><span class="sxs-lookup"><span data-stu-id="986e2-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="986e2-114">如果 Schannel 發現此屬性集，則不會使用 CERT \_ KEY \_ >prov \_ INFO \_ \_ 屬性 ID 屬性。</span><span class="sxs-lookup"><span data-stu-id="986e2-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="986e2-115">伺服器私密金鑰</span><span class="sxs-lookup"><span data-stu-id="986e2-115">Server Private Keys</span></span>

<span data-ttu-id="986e2-116">伺服器私密金鑰是由下列其中一項 Csp 所儲存：</span><span class="sxs-lookup"><span data-stu-id="986e2-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="986e2-117">>PROV \_ RSA \_ SCHANNEL</span><span class="sxs-lookup"><span data-stu-id="986e2-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="986e2-118">>PROV \_ DH \_ SCHANNEL</span><span class="sxs-lookup"><span data-stu-id="986e2-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="986e2-119">>PROV \_ FORTEZZA CSP</span><span class="sxs-lookup"><span data-stu-id="986e2-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="986e2-120">CSP 的選擇取決於所選的 [*金鑰交換演算法*](/windows/desktop/SecGloss/k-gly)。</span><span class="sxs-lookup"><span data-stu-id="986e2-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="986e2-121">伺服器私用金鑰的類型必須是 \_ KEYEXCHANGE。</span><span class="sxs-lookup"><span data-stu-id="986e2-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 
