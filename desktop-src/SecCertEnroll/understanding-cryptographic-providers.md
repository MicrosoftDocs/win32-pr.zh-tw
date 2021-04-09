---
description: 提供者會執行密碼編譯演算法、產生金鑰、提供金鑰儲存，以及驗證使用者。 提供者可在硬體、軟體或兩者中執行。
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: 瞭解密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944806"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="d8ebc-104">瞭解密碼編譯提供者</span><span class="sxs-lookup"><span data-stu-id="d8ebc-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="d8ebc-105">在密碼編譯 API 中引進的密碼編譯提供者概念 ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) ，而且在 [*密碼編譯 api：新一代*](/windows/desktop/SecGloss/c-gly) (CNG) 是在 Microsoft 作業系統上安全地執行密碼編譯功能的核心。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="d8ebc-106">這兩個 Sdk 用來建立許多應用程式，並由其他 Sdk 在內部呼叫。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="d8ebc-107">例如，Active Directory 憑證服務和憑證註冊 API 依賴 CryptoAPI 和 CNG。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="d8ebc-108">一般而言，提供者會執行密碼編譯演算法、產生金鑰、提供金鑰儲存，以及驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="d8ebc-109">提供者可在硬體、軟體或兩者中執行。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="d8ebc-110">使用 CryptoAPI 或 CNG 所建立的應用程式無法改變提供者所建立的金鑰，也無法改變密碼編譯演算法的執行。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="d8ebc-111">Microsoft 所建立的多個提供者會與作業系統一起散發。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="d8ebc-112">其他提供者已由協力廠商建立和散發。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="d8ebc-113">下列主題強調與 CryptoAPI 相關聯的提供者之間的差異，以及與 CNG 相關聯的提供者。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="d8ebc-114">一般而言，本檔會參考提供者，而不需要參考與其相關聯的 SDK，請注意關聯性。</span><span class="sxs-lookup"><span data-stu-id="d8ebc-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="d8ebc-115">CryptoAPI 密碼編譯服務提供者</span><span class="sxs-lookup"><span data-stu-id="d8ebc-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="d8ebc-116">CNG 密碼編譯演算法提供者</span><span class="sxs-lookup"><span data-stu-id="d8ebc-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="d8ebc-117">CNG 金鑰儲存提供者</span><span class="sxs-lookup"><span data-stu-id="d8ebc-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="d8ebc-118">列舉已安裝的提供者</span><span class="sxs-lookup"><span data-stu-id="d8ebc-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="d8ebc-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8ebc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8ebc-120">使用憑證註冊 API</span><span class="sxs-lookup"><span data-stu-id="d8ebc-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
