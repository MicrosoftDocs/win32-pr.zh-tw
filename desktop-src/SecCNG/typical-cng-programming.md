---
description: CNG API 會執行可延伸的提供者模型，可讓您指定所需的密碼編譯演算法，而不是特定的提供者，以載入提供者。
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: 一般 CNG 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1119da63ca1ea0613444b150914c06664f36c121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690507"
---
# <a name="typical-cng-programming"></a><span data-ttu-id="bdfbd-103">一般 CNG 程式設計</span><span class="sxs-lookup"><span data-stu-id="bdfbd-103">Typical CNG Programming</span></span>

<span data-ttu-id="bdfbd-104">CNG API 會執行可延伸的提供者模型，可讓您指定所需的密碼編譯演算法，而不是特定的提供者，以載入提供者。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-104">The CNG API implements an extensible provider model that lets you load a provider by specifying the required cryptographic algorithm rather than a particular provider.</span></span> <span data-ttu-id="bdfbd-105">優點是可以取代或升級演算法提供者，而且您不需要以任何方式變更程式碼，就能使用新的提供者。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-105">The advantage is that an algorithm provider can be replaced or upgraded and you will not have to change your code in any way to use the new provider.</span></span> <span data-ttu-id="bdfbd-106">此外，如果某些演算法在未來判斷為不安全，則可以安裝該演算法的安全版本，而不會影響您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-106">Also, if some algorithm is determined to be unsafe in the future, a more secure version of that algorithm can be installed without affecting your code.</span></span> <span data-ttu-id="bdfbd-107">大部分的 CNG Api 都需要提供者或提供者所建立的物件。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-107">Most of the CNG APIs require a provider or an object created by a provider.</span></span>

<span data-ttu-id="bdfbd-108">使用 CNG API 進行密碼編譯基本作業時所牽涉到的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="bdfbd-108">The typical steps involved in using the CNG API for cryptographic primitive operations are as follows:</span></span>

1.  <span data-ttu-id="bdfbd-109">開啟演算法提供者</span><span class="sxs-lookup"><span data-stu-id="bdfbd-109">Opening the Algorithm Provider</span></span>
2.  <span data-ttu-id="bdfbd-110">取得或設定演算法屬性</span><span class="sxs-lookup"><span data-stu-id="bdfbd-110">Getting or Setting Algorithm Properties</span></span>
3.  <span data-ttu-id="bdfbd-111">建立或匯入金鑰</span><span class="sxs-lookup"><span data-stu-id="bdfbd-111">Creating or Importing a Key</span></span>
4.  <span data-ttu-id="bdfbd-112">執行密碼編譯作業</span><span class="sxs-lookup"><span data-stu-id="bdfbd-112">Performing Cryptographic Operations</span></span>
5.  <span data-ttu-id="bdfbd-113">關閉演算法提供者</span><span class="sxs-lookup"><span data-stu-id="bdfbd-113">Closing the Algorithm Provider</span></span>

<span data-ttu-id="bdfbd-114">如需詳細資訊，請參閱程式設計範例。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-114">For more information, see Programming Examples.</span></span>

## <a name="opening-the-algorithm-provider"></a><span data-ttu-id="bdfbd-115">開啟演算法提供者</span><span class="sxs-lookup"><span data-stu-id="bdfbd-115">Opening the Algorithm Provider</span></span>

<span data-ttu-id="bdfbd-116">[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)函式會為您提供用於後續 CNG api 的演算法提供者控制碼，例如 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)或 [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-116">The [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function provides you with an algorithm provider handle that is used in subsequent CNG APIs, such as [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) or [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair).</span></span>

## <a name="getting-or-setting-algorithm-properties"></a><span data-ttu-id="bdfbd-117">取得或設定演算法屬性</span><span class="sxs-lookup"><span data-stu-id="bdfbd-117">Getting or Setting Algorithm Properties</span></span>

<span data-ttu-id="bdfbd-118">您可以使用演算法提供者控制碼來取得演算法的實作為詳細資料，例如金鑰大小或目前的作業模式。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-118">You can use the algorithm provider handle to get implementation details for the algorithm, such as the key size or the current mode of operation.</span></span> <span data-ttu-id="bdfbd-119">您可以使用 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函數來取得特定屬性。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-119">You use the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to obtain specific properties.</span></span>

<span data-ttu-id="bdfbd-120">您也可以修改演算法的屬性。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-120">You can also modify the properties of the algorithm.</span></span> <span data-ttu-id="bdfbd-121">例如，如果您想要將 ECB 區塊加密連結與 AES 搭配使用，您可以將 AES 演算法的 **BCRYPT \_ 鏈式 \_ 模式** 屬性設定為 **BCRYPT \_ 鏈 \_ 模式 \_ ECB**; 此屬性會指派給使用此演算法控制碼建立的所有 AES 金鑰，而不需要設定每個 aes 金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-121">For example, If you want to use ECB block cipher chaining with AES, you set the **BCRYPT\_CHAINING\_MODE** property of an AES algorithm to **BCRYPT\_CHAIN\_MODE\_ECB**; the property is assigned to all AES keys created using this algorithm handle, without the need to configure each and every AES key.</span></span> <span data-ttu-id="bdfbd-122">您可以使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 函數來修改這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-122">You use the [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) function to modify these properties.</span></span>

## <a name="creating-or-importing-a-key"></a><span data-ttu-id="bdfbd-123">建立或匯入金鑰</span><span class="sxs-lookup"><span data-stu-id="bdfbd-123">Creating or Importing a Key</span></span>

<span data-ttu-id="bdfbd-124">視您使用的演算法類型而定，您可能需要建立或載入金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-124">Depending on the type of algorithm you use, you may need to create or load a key.</span></span> <span data-ttu-id="bdfbd-125">例如， [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) 函式會接受第一個參數的按鍵控制碼。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-125">For example, the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function takes a key handle for the first parameter.</span></span> <span data-ttu-id="bdfbd-126">如果您希望該函式使用對稱式加密演算法（例如 AES）來加密資料，您必須先取得金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-126">If you want that function to encrypt data with a symmetric encryption algorithm such as AES, you must first obtain a key.</span></span> <span data-ttu-id="bdfbd-127">您取得金鑰的方式取決於所使用的演算法類型和金鑰的來源。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-127">How you obtain the key depends on the type of algorithm being used and the source of the key.</span></span>

<span data-ttu-id="bdfbd-128">您可以使用 [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) 和 [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) 函數來建立暫時金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-128">You can create ephemeral keys with the [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) and [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) functions.</span></span> <span data-ttu-id="bdfbd-129">您也可以使用 [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) 和 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 函數，從記憶體 BLOB 匯入暫時金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-129">You can also import ephemeral keys from a memory BLOB with the [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) and [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) functions.</span></span>

<span data-ttu-id="bdfbd-130">針對保存的金鑰，您可以使用金鑰儲存功能來載入金鑰儲存提供者，然後建立或載入金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-130">For persisted keys, you use the key storage functions to load a key storage provider, and then create or load the keys.</span></span> <span data-ttu-id="bdfbd-131">您也可以使用這些函式，藉由傳遞任何容器名稱的 **Null** 來建立或載入暫時金鑰。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-131">You can also use these functions to create or load ephemeral keys by passing **NULL** for any container names.</span></span> <span data-ttu-id="bdfbd-132">如需金鑰儲存功能的詳細資訊，請參閱 [CNG 金鑰儲存功能](cng-key-storage-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-132">For more information about the key storage functions, see [CNG Key Storage Functions](cng-key-storage-functions.md).</span></span>

## <a name="performing-cryptographic-operations"></a><span data-ttu-id="bdfbd-133">執行密碼編譯作業</span><span class="sxs-lookup"><span data-stu-id="bdfbd-133">Performing Cryptographic Operations</span></span>

<span data-ttu-id="bdfbd-134">您現在已準備好執行密碼編譯作業，例如分別使用 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) 或 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) 函數來加密或解密資料。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-134">You are now ready to perform the cryptographic operation, such as encrypting or decrypting data by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) or [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) functions, respectively.</span></span>

## <a name="closing-the-algorithm-provider"></a><span data-ttu-id="bdfbd-135">關閉演算法提供者</span><span class="sxs-lookup"><span data-stu-id="bdfbd-135">Closing the Algorithm Provider</span></span>

<span data-ttu-id="bdfbd-136">當不再需要提供者時，您必須將控制碼傳遞至 [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) 函式來關閉提供者。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-136">When the provider is no longer needed, you must pass the handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function to close the provider.</span></span> <span data-ttu-id="bdfbd-137">這會導致提供者釋放已配置給該演算法提供者實例的任何資源。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-137">This causes the provider to release any resources that have been allocated for that algorithm provider instance.</span></span> <span data-ttu-id="bdfbd-138">提供者控制碼關閉之後，就無法重複使用。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-138">After a provider handle is closed, it cannot be reused.</span></span>

<span data-ttu-id="bdfbd-139">載入提供者可能是相當耗時的進程。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-139">Loading a provider can be a relatively time-intensive process.</span></span> <span data-ttu-id="bdfbd-140">因此，您應該在應用程式的存留期期間，快取您將參考多次的提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-140">You should therefore cache any provider handles that you will reference multiple times during the lifetime of your application.</span></span>

## <a name="programming-examples"></a><span data-ttu-id="bdfbd-141">程式設計範例</span><span class="sxs-lookup"><span data-stu-id="bdfbd-141">Programming Examples</span></span>

<span data-ttu-id="bdfbd-142">下列範例說明如何使用 CNG 執行特定的密碼編譯作業。</span><span class="sxs-lookup"><span data-stu-id="bdfbd-142">The following examples describe how to perform specific cryptographic operations using CNG.</span></span>

-   [<span data-ttu-id="bdfbd-143">使用 CNG 建立雜湊</span><span class="sxs-lookup"><span data-stu-id="bdfbd-143">Creating a Hash with CNG</span></span>](creating-a-hash-with-cng.md)
-   [<span data-ttu-id="bdfbd-144">使用 CNG 簽署資料</span><span class="sxs-lookup"><span data-stu-id="bdfbd-144">Signing Data with CNG</span></span>](signing-data-with-cng.md)
-   [<span data-ttu-id="bdfbd-145">使用 CNG 加密資料</span><span class="sxs-lookup"><span data-stu-id="bdfbd-145">Encrypting Data with CNG</span></span>](encrypting-data-with-cng.md)

 

 



