---
description: 文字或其他位元組字串的雜湊是相關的、統計唯一、固定長度的值。
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: 資料雜湊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852311"
---
# <a name="data-hashes"></a><span data-ttu-id="9792f-103">資料雜湊</span><span class="sxs-lookup"><span data-stu-id="9792f-103">Data Hashes</span></span>

<span data-ttu-id="9792f-104">文字或其他位元組字串的 [*雜湊*](../secgloss/h-gly.md) 是相關的、統計唯一、固定長度的值。</span><span class="sxs-lookup"><span data-stu-id="9792f-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="9792f-105">在某些檔中，文字的 *雜湊* 也稱為摘要;不過，在本檔中，一律會使用「雜湊」一詞。</span><span class="sxs-lookup"><span data-stu-id="9792f-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="9792f-106">CryptoAPI 函式提供一種方法來建立任何文字或其他位元組字串的雜湊。</span><span class="sxs-lookup"><span data-stu-id="9792f-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="9792f-107">然後，該雜湊就可以用來作為其相關資料的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9792f-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="9792f-108">為了確保文字的 [*完整性*](../secgloss/i-gly.md) ，文字的 [*雜湊*](../secgloss/h-gly.md) 可以隨文字一起傳送。</span><span class="sxs-lookup"><span data-stu-id="9792f-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="9792f-109">然後接收者可以計算所收到資料的雜湊，並比較以接收的雜湊計算的雜湊。</span><span class="sxs-lookup"><span data-stu-id="9792f-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="9792f-110">如果兩者相符，則接收的資料必須與建立所接收雜湊的資料相同。</span><span class="sxs-lookup"><span data-stu-id="9792f-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="9792f-111">若要取得雜湊值，請使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)建立雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="9792f-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="9792f-112">此物件將累積要驗證的資料。</span><span class="sxs-lookup"><span data-stu-id="9792f-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="9792f-113">然後使用 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) 函式，將資料新增至雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="9792f-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="9792f-114">將最後一個資料區塊新增至雜湊之後， [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) 函數會用來取得資料的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="9792f-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="9792f-115">一旦取得雜湊值，就會以 [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) 終結雜湊物件，以提供更佳的安全性。</span><span class="sxs-lookup"><span data-stu-id="9792f-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
