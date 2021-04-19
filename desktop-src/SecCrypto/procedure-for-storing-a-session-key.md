---
description: 說明用於儲存工作階段金鑰的程式。
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: 儲存工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977347"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="b5eef-103">儲存工作階段金鑰</span><span class="sxs-lookup"><span data-stu-id="b5eef-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="b5eef-104">本節假設使用者擁有一組 [*公開/私密金鑰*](../secgloss/p-gly.md)組。</span><span class="sxs-lookup"><span data-stu-id="b5eef-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="b5eef-105">如需建立金鑰組的指示和範例，請參閱 [範例 C 程式：建立金鑰容器和產生金鑰](example-c-program-creating-a-key-container-and-generating-keys.md)。</span><span class="sxs-lookup"><span data-stu-id="b5eef-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="b5eef-106">**若要儲存工作階段金鑰**</span><span class="sxs-lookup"><span data-stu-id="b5eef-106">**To store a session key**</span></span>

1.  <span data-ttu-id="b5eef-107">使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)函數建立簡單的 [*金鑰 BLOB*](../secgloss/k-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b5eef-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="b5eef-108">這會將工作階段金鑰從 CSP 傳送至應用程式的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="b5eef-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="b5eef-109">指定用來簽署金鑰 BLOB 的交換公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="b5eef-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="b5eef-110">將簽署的金鑰 BLOB 儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="b5eef-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="b5eef-111">假設所有磁片都不是安全的。</span><span class="sxs-lookup"><span data-stu-id="b5eef-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="b5eef-112">需要金鑰時，請從磁片讀取金鑰 BLOB。</span><span class="sxs-lookup"><span data-stu-id="b5eef-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="b5eef-113">使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式，將金鑰 BLOB 匯入回 CSP。</span><span class="sxs-lookup"><span data-stu-id="b5eef-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="b5eef-114">如需建立 [*工作階段金鑰*](../secgloss/s-gly.md) ，並將該金鑰匯出至可寫入磁片檔案之 [*簡單金鑰 BLOB*](../secgloss/s-gly.md) 的範例，請參閱 [範例 C 程式：匯出工作階段金鑰](example-c-program-exporting-a-session-key.md)。</span><span class="sxs-lookup"><span data-stu-id="b5eef-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="b5eef-115">此程式只提供基本的安全性。</span><span class="sxs-lookup"><span data-stu-id="b5eef-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="b5eef-116">如果預存工作階段金鑰稍後將用來加密資料，則先前的程式並不會提供足夠的安全性。</span><span class="sxs-lookup"><span data-stu-id="b5eef-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="b5eef-117">若要提供更高的安全性，請使用 exchange 私密金鑰簽署金鑰 BLOB，然後再將其儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="b5eef-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="b5eef-118">當金鑰 BLOB 稍後從磁片讀取時，就可以驗證其簽章，以確保金鑰 BLOB 保持不變。</span><span class="sxs-lookup"><span data-stu-id="b5eef-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="b5eef-119">如果金鑰 BLOB 未簽署，可以存取磁片或儲存金鑰之其他媒體的任何人，都可以建立新的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="b5eef-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="b5eef-120">您可以使用原始使用者的 [*公開金鑰*](../secgloss/p-gly.md)[*交換金鑰*](../secgloss/e-gly.md)來加密新的工作階段金鑰，而這個新的金鑰可以替代為原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="b5eef-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="b5eef-121">如果使用者在不知情的情況下使用替代的工作階段金鑰來加密檔案和訊息，則建立替代金鑰的人員可以輕鬆地將它們解密。</span><span class="sxs-lookup"><span data-stu-id="b5eef-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="b5eef-122">[雜湊和數位簽章](hashes-and-digital-signatures.md)中會詳細討論數位簽章。</span><span class="sxs-lookup"><span data-stu-id="b5eef-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
