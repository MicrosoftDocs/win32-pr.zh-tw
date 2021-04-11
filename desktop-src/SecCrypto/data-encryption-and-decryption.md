---
description: 加密是指將純文字資料 (純文字) 轉換成看似隨機且無意義 (加密文字) 的程式。 解密是將加密文字轉換回純文字的程式。
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: 資料加密和解密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112676"
---
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="95090-104">資料加密和解密</span><span class="sxs-lookup"><span data-stu-id="95090-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="95090-105">加密是指將純文字資料 ([*純*](../secgloss/p-gly.md) 文本) 轉換成看似隨機且無意義 ([*加密*](../secgloss/c-gly.md) 文字) 的程式。</span><span class="sxs-lookup"><span data-stu-id="95090-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="95090-106">解密是將加密文字轉換回純文字的程式。</span><span class="sxs-lookup"><span data-stu-id="95090-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="95090-107">若要加密超過少量的資料，請使用 [*對稱式加密*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="95090-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="95090-108">[*對稱金鑰*](../secgloss/s-gly.md)是在加密和解密程式期間使用。</span><span class="sxs-lookup"><span data-stu-id="95090-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="95090-109">若要將特定的加密文字片段解密，必須使用用來加密資料的金鑰。</span><span class="sxs-lookup"><span data-stu-id="95090-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="95090-110">每個加密演算法的目標是要讓它盡可能難以解密所產生的加密文字，而不使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="95090-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="95090-111">如果使用的是很好的加密演算法，則在每個可能的索引鍵中，都不會有明顯的技巧。</span><span class="sxs-lookup"><span data-stu-id="95090-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="95090-112">針對這樣的演算法，索引鍵越長，就越難解密加密文字片段，而不需要擁有金鑰。</span><span class="sxs-lookup"><span data-stu-id="95090-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="95090-113">很難判斷加密演算法的品質。</span><span class="sxs-lookup"><span data-stu-id="95090-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="95090-114">如果有適當的攻擊，則看起來的演算法有時會很容易中斷。</span><span class="sxs-lookup"><span data-stu-id="95090-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="95090-115">選取加密演算法時，最好選擇已在使用中的帳戶，並成功 resisted 所有攻擊。</span><span class="sxs-lookup"><span data-stu-id="95090-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="95090-116">如需詳細資訊，請參閱 [資料加密和解密功能](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="95090-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
