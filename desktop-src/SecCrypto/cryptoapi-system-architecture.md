---
description: 說明 CryptoAPI 系統架構。
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: CryptoAPI 系統架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318232"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="0d76c-103">CryptoAPI 系統架構</span><span class="sxs-lookup"><span data-stu-id="0d76c-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="0d76c-104">CryptoAPI 系統架構由五個主要功能區域組成：</span><span class="sxs-lookup"><span data-stu-id="0d76c-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="0d76c-105">基底加密函式</span><span class="sxs-lookup"><span data-stu-id="0d76c-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="0d76c-106">憑證編碼/解碼函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="0d76c-107">憑證存放區功能</span><span class="sxs-lookup"><span data-stu-id="0d76c-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="0d76c-108">簡化的訊息函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="0d76c-109">低層級訊息函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="0d76c-110">基底加密函式</span><span class="sxs-lookup"><span data-stu-id="0d76c-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="0d76c-111">用來連接到 CSP 的 *內容* 函式。</span><span class="sxs-lookup"><span data-stu-id="0d76c-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="0d76c-112">這些函式可讓應用程式依名稱選擇特定的 CSP，或選擇可提供所需功能類別的特定 CSP。</span><span class="sxs-lookup"><span data-stu-id="0d76c-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="0d76c-113">用來產生及儲存 [*密碼編譯金鑰*](../secgloss/c-gly.md)的 [*金鑰產生函數*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="0d76c-114">包含變更 [*連結模式*](../secgloss/c-gly.md)、 [*初始化向量*](../secgloss/i-gly.md)和其他加密功能的完整支援。</span><span class="sxs-lookup"><span data-stu-id="0d76c-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="0d76c-115">如需詳細資訊，請參閱 [金鑰產生和 Exchange 功能](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="0d76c-116">用來交換或傳輸金鑰的 *金鑰交換函數*。</span><span class="sxs-lookup"><span data-stu-id="0d76c-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="0d76c-117">如需詳細資訊，請參閱 [密碼編譯金鑰儲存和交換](cryptographic-key-storage-and-exchange.md) 和 [金鑰產生和 exchange 功能](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="0d76c-118">憑證編碼/解碼函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="0d76c-119">用來加密或解密資料的函數。</span><span class="sxs-lookup"><span data-stu-id="0d76c-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="0d76c-120">[*雜湊*](../secgloss/h-gly.md)資料也包含支援。</span><span class="sxs-lookup"><span data-stu-id="0d76c-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="0d76c-121">如需詳細資訊，請參閱 [資料加密和解密功能](cryptography-functions.md) 以及 [資料加密和解密](data-encryption-and-decryption.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="0d76c-122">憑證存放區功能</span><span class="sxs-lookup"><span data-stu-id="0d76c-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="0d76c-123">用來管理數位憑證集合的函式。</span><span class="sxs-lookup"><span data-stu-id="0d76c-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="0d76c-124">如需詳細資訊，請參閱 [數位憑證](digital-certificates.md) 和 [憑證存放區功能](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="0d76c-125">簡化的訊息函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="0d76c-126">用來加密和解密訊息和資料的函式。</span><span class="sxs-lookup"><span data-stu-id="0d76c-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="0d76c-127">用來簽署訊息和資料的函式。</span><span class="sxs-lookup"><span data-stu-id="0d76c-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="0d76c-128">用來確認收到的訊息和相關資料之簽章真實性的函數。</span><span class="sxs-lookup"><span data-stu-id="0d76c-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="0d76c-129">如需詳細資訊，請參閱 [簡化的訊息](simplified-messages.md) 和 [簡化的訊息函數](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="0d76c-130">低層級訊息函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="0d76c-131">用來執行簡化訊息函數所執行之所有工作的函數。</span><span class="sxs-lookup"><span data-stu-id="0d76c-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="0d76c-132">低層級的訊息函式比簡化的訊息函式提供更大的彈性，但需要更多函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="0d76c-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="0d76c-133">如需詳細資訊，請參閱 [低層級訊息](low-level-messages.md) 和 [低層級訊息函數](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0d76c-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![cryptoapi 架構](images/cryparch.png)

<span data-ttu-id="0d76c-135">每個功能區域的函式名稱中都有一個關鍵字，指出其功能區域。</span><span class="sxs-lookup"><span data-stu-id="0d76c-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="0d76c-136">功能區域</span><span class="sxs-lookup"><span data-stu-id="0d76c-136">Functional area</span></span>              | <span data-ttu-id="0d76c-137">函數名稱慣例</span><span class="sxs-lookup"><span data-stu-id="0d76c-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="0d76c-138">基底加密函式</span><span class="sxs-lookup"><span data-stu-id="0d76c-138">Base cryptographic functions</span></span> | <span data-ttu-id="0d76c-139">地穴</span><span class="sxs-lookup"><span data-stu-id="0d76c-139">Crypt</span></span>                    |
| <span data-ttu-id="0d76c-140">編碼/解碼函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="0d76c-141">地穴</span><span class="sxs-lookup"><span data-stu-id="0d76c-141">Crypt</span></span>                    |
| <span data-ttu-id="0d76c-142">憑證存放區功能</span><span class="sxs-lookup"><span data-stu-id="0d76c-142">Certificate store functions</span></span>  | <span data-ttu-id="0d76c-143">市集</span><span class="sxs-lookup"><span data-stu-id="0d76c-143">Store</span></span>                    |
| <span data-ttu-id="0d76c-144">簡化的訊息函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-144">Simplified message functions</span></span> | <span data-ttu-id="0d76c-145">訊息</span><span class="sxs-lookup"><span data-stu-id="0d76c-145">Message</span></span>                  |
| <span data-ttu-id="0d76c-146">低層級訊息函數</span><span class="sxs-lookup"><span data-stu-id="0d76c-146">Low-level message functions</span></span>  | <span data-ttu-id="0d76c-147">Msg</span><span class="sxs-lookup"><span data-stu-id="0d76c-147">Msg</span></span>                      |



 

<span data-ttu-id="0d76c-148">應用程式會在所有這些區域中使用函數。</span><span class="sxs-lookup"><span data-stu-id="0d76c-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="0d76c-149">這些函式會結合在一起，以執行 CryptoAPI。</span><span class="sxs-lookup"><span data-stu-id="0d76c-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="0d76c-150">[*基底加密*](../secgloss/b-gly.md)函式會使用 csp 來取得必要的密碼編譯演算法，以及 [加密金鑰](cryptographic-keys.md)的產生和安全儲存。</span><span class="sxs-lookup"><span data-stu-id="0d76c-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="0d76c-151">使用兩種不同的密碼編譯金鑰： [*工作階段金鑰*](../secgloss/s-gly.md)（用於單一加密/解密）和 [*公開/私密金鑰*](../secgloss/p-gly.md)組（會以更永久的方式使用）。</span><span class="sxs-lookup"><span data-stu-id="0d76c-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="0d76c-152">雖然應用程式可以直接與五個功能區域中的任一個通訊，但無法與 CSP 直接通訊。</span><span class="sxs-lookup"><span data-stu-id="0d76c-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="0d76c-153">所有應用程式對 CSP 的通訊都是透過 [*基底加密*](../secgloss/b-gly.md)函式進行。</span><span class="sxs-lookup"><span data-stu-id="0d76c-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="0d76c-154">基底加密函式具有參數，可指定要使用的 CSP。</span><span class="sxs-lookup"><span data-stu-id="0d76c-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="0d76c-155">此參數可以設定為 **Null** ，以選取預設的 CSP。</span><span class="sxs-lookup"><span data-stu-id="0d76c-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
