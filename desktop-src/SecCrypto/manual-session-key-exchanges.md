---
description: 顯示如何傳送加密的訊息。
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: 手動工作階段金鑰交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567258"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="77a0c-103">手動工作階段金鑰交換</span><span class="sxs-lookup"><span data-stu-id="77a0c-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="77a0c-104">本節所述的程式假設使用者 (或 CryptoAPI 用戶端) 已經有自己的一組 [*公開/私密金鑰*](../secgloss/p-gly.md) 組，而且也取得彼此的 [*公開金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="77a0c-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="77a0c-105">下圖顯示如何使用此程式來傳送加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="77a0c-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![傳送加密的訊息](images/capi04.png)

<span data-ttu-id="77a0c-107">這種方法很容易受到一種常見的攻擊。</span><span class="sxs-lookup"><span data-stu-id="77a0c-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="77a0c-108">小人可以取得一或多個加密訊息和加密金鑰的複本。</span><span class="sxs-lookup"><span data-stu-id="77a0c-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="77a0c-109">然後，在稍後的時間，小人可以將其中一個訊息傳送給接收者，而接收者將無法得知訊息未直接來自原始寄件者。</span><span class="sxs-lookup"><span data-stu-id="77a0c-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="77a0c-110">您可以使用時間戳所有訊息或使用序號來降低這項風險。</span><span class="sxs-lookup"><span data-stu-id="77a0c-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="77a0c-111">將加密的訊息傳送給另一位使用者的最簡單方式，就是傳送以隨機工作階段金鑰加密的訊息，以及使用接收者的 [*金鑰交換公開金鑰*](../secgloss/k-gly.md)加密的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="77a0c-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="77a0c-112">以下是傳送加密工作階段金鑰的步驟。</span><span class="sxs-lookup"><span data-stu-id="77a0c-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="77a0c-113">**傳送加密的工作階段金鑰**</span><span class="sxs-lookup"><span data-stu-id="77a0c-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="77a0c-114">使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)函式來建立隨機 [*工作階段金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="77a0c-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="77a0c-115">使用工作階段金鑰來加密訊息。</span><span class="sxs-lookup"><span data-stu-id="77a0c-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="77a0c-116">這項程式會在 [資料加密和解密](data-encryption-and-decryption.md)中討論。</span><span class="sxs-lookup"><span data-stu-id="77a0c-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="77a0c-117">使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)函式將工作階段金鑰匯出至 [*金鑰 BLOB*](../secgloss/k-gly.md) ，並指定使用目的地使用者的金鑰交換公開金鑰來加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="77a0c-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="77a0c-118">將加密的訊息和加密的金鑰 BLOB 傳送給目的地使用者。</span><span class="sxs-lookup"><span data-stu-id="77a0c-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="77a0c-119">目的地使用者使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式，將金鑰 BLOB 匯入其 CSP 中。</span><span class="sxs-lookup"><span data-stu-id="77a0c-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="77a0c-120">如果在步驟3中指定了目的地使用者的金鑰交換公開金鑰，這將會自動將工作階段金鑰解密。</span><span class="sxs-lookup"><span data-stu-id="77a0c-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="77a0c-121">目的地使用者接著可以使用工作階段金鑰來解密訊息， [並遵循資料加密和解密](data-encryption-and-decryption.md)中所討論的程式。</span><span class="sxs-lookup"><span data-stu-id="77a0c-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
