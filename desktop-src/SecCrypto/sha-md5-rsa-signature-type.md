---
description: '>PROV RSA 安全通道的 Csp \_ \_ 必須支援 CALG \_ SSL3 \_ SHAMD5 雜湊，此雜湊可與 SSL 3.0 和 TLS 1.0 用戶端驗證中使用的 Microsoft 基礎密碼編譯提供者相容。'
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: SHA/MD5 RSA 簽章類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970752"
---
# <a name="shamd5-rsa-signature-type"></a><span data-ttu-id="55262-103">SHA/MD5 RSA 簽章類型</span><span class="sxs-lookup"><span data-stu-id="55262-103">SHA/MD5 RSA Signature Type</span></span>

<span data-ttu-id="55262-104">>PROV RSA 安全通道的 Csp \_ \_ 必須支援 CALG \_ SSL3 \_ SHAMD5 [*雜湊，此雜湊*](../secgloss/h-gly.md) 可與 SSL 3.0 和 TLS 1.0 用戶端驗證中使用的 Microsoft 基礎密碼編譯提供者相容。</span><span class="sxs-lookup"><span data-stu-id="55262-104">CSPs for PROV\_RSA\_SCHANNEL must support the CALG\_SSL3\_SHAMD5 [*hash*](../secgloss/h-gly.md) that is compatible with the Microsoft Base Cryptographic Provider used in SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="55262-105">此雜湊包含 [*MD5*](../secgloss/m-gly.md) 雜湊的串連，以及使用 RSA 或 Diffie-Hellman 私密金鑰所簽署的 SHA 雜湊。</span><span class="sxs-lookup"><span data-stu-id="55262-105">This hash consists of a concatenation of an [*MD5*](../secgloss/m-gly.md) hash and a SHA hash signed with an RSA or Diffie-Hellman private key.</span></span> <span data-ttu-id="55262-106">使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) 或 [**CPCREATEHASH**](https://www.bing.com/search?q=**CPCreateHash**) 函數搭配 CALG \_ SSL3 \_ SHAMD5 作為 *Algid* 參數，即可建立此類型雜湊值的控制碼。</span><span class="sxs-lookup"><span data-stu-id="55262-106">A handle to a hash value of this type is created by using the [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) or [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) function with CALG\_SSL3\_SHAMD5 as the *Algid* parameter.</span></span> <span data-ttu-id="55262-107">如需使用雜湊函式的範例，請見 [c 程式：建立和雜湊工作階段金鑰](example-c-program-creating-and-hashing-a-session-key.md) ，以及 [範例 c 程式：簽署雜湊和驗證雜湊簽](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md)章。</span><span class="sxs-lookup"><span data-stu-id="55262-107">Examples of using hash functions can be seen in [Example C Program: Creating and Hashing a Session Key](example-c-program-creating-and-hashing-a-session-key.md) and [Example C Program: Signing a Hash and Verifying the Hash Signature](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span></span>

 

 
