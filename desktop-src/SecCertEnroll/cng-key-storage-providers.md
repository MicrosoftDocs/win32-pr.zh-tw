---
description: 不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者分開 (Ksp) 。
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: CNG 金鑰儲存提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386096"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="5a12c-103">CNG 金鑰儲存提供者</span><span class="sxs-lookup"><span data-stu-id="5a12c-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="5a12c-104">不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者分開 (Ksp) 。</span><span class="sxs-lookup"><span data-stu-id="5a12c-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="5a12c-105">Ksp 可以用來建立、刪除、匯出、匯入、開啟和儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="5a12c-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="5a12c-106">根據執行的不同，它們也可以用於非對稱式加密、秘密合約和簽署。</span><span class="sxs-lookup"><span data-stu-id="5a12c-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="5a12c-107">從 Windows Vista 和 Windows Server 2008 開始，Microsoft 會安裝下列 Ksp。</span><span class="sxs-lookup"><span data-stu-id="5a12c-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5a12c-108">廠商可以建立和安裝其他提供者。</span><span class="sxs-lookup"><span data-stu-id="5a12c-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="5a12c-109">Microsoft 軟體金鑰儲存提供者</span><span class="sxs-lookup"><span data-stu-id="5a12c-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="5a12c-110">支援軟體金鑰建立和儲存，以及下列演算法。</span><span class="sxs-lookup"><span data-stu-id="5a12c-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="5a12c-111">演算法</span><span class="sxs-lookup"><span data-stu-id="5a12c-111">Algorithm</span></span>                                          | <span data-ttu-id="5a12c-112">目的</span><span class="sxs-lookup"><span data-stu-id="5a12c-112">Purpose</span></span>                           | <span data-ttu-id="5a12c-113">金鑰長度 (bits) </span><span class="sxs-lookup"><span data-stu-id="5a12c-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="5a12c-114">Diffie-Hellman (DH) </span><span class="sxs-lookup"><span data-stu-id="5a12c-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="5a12c-115">秘密合約和金鑰交換</span><span class="sxs-lookup"><span data-stu-id="5a12c-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="5a12c-116">512至4096以64位遞增</span><span class="sxs-lookup"><span data-stu-id="5a12c-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="5a12c-117"> (DSA) 的數位簽章演算法</span><span class="sxs-lookup"><span data-stu-id="5a12c-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="5a12c-118">簽章</span><span class="sxs-lookup"><span data-stu-id="5a12c-118">Signatures</span></span>                        | <span data-ttu-id="5a12c-119">512至1024以64位遞增</span><span class="sxs-lookup"><span data-stu-id="5a12c-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="5a12c-120"> (ECDH) 的橢圓曲線 Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="5a12c-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="5a12c-121">秘密合約和金鑰交換</span><span class="sxs-lookup"><span data-stu-id="5a12c-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="5a12c-122">P256、P384、P521</span><span class="sxs-lookup"><span data-stu-id="5a12c-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5a12c-123"> (ECDSA) 的橢圓曲線數位簽章演算法</span><span class="sxs-lookup"><span data-stu-id="5a12c-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="5a12c-124">簽章</span><span class="sxs-lookup"><span data-stu-id="5a12c-124">Signatures</span></span>                        | <span data-ttu-id="5a12c-125">P256、P384、P521</span><span class="sxs-lookup"><span data-stu-id="5a12c-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5a12c-126">RSA</span><span class="sxs-lookup"><span data-stu-id="5a12c-126">RSA</span></span>                                                | <span data-ttu-id="5a12c-127">非對稱式加密和簽署</span><span class="sxs-lookup"><span data-stu-id="5a12c-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="5a12c-128">512至16384以64位遞增</span><span class="sxs-lookup"><span data-stu-id="5a12c-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="5a12c-129">Microsoft 智慧卡金鑰儲存提供者</span><span class="sxs-lookup"><span data-stu-id="5a12c-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="5a12c-130">支援智慧卡金鑰建立和儲存，以及下列演算法。</span><span class="sxs-lookup"><span data-stu-id="5a12c-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="5a12c-131">演算法</span><span class="sxs-lookup"><span data-stu-id="5a12c-131">Algorithm</span></span>                                          | <span data-ttu-id="5a12c-132">目的</span><span class="sxs-lookup"><span data-stu-id="5a12c-132">Purpose</span></span>                           | <span data-ttu-id="5a12c-133">金鑰長度 (bits) </span><span class="sxs-lookup"><span data-stu-id="5a12c-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="5a12c-134">Diffie-Hellman (DH) </span><span class="sxs-lookup"><span data-stu-id="5a12c-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="5a12c-135">秘密合約和金鑰交換</span><span class="sxs-lookup"><span data-stu-id="5a12c-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="5a12c-136">512至4096以64位遞增</span><span class="sxs-lookup"><span data-stu-id="5a12c-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="5a12c-137"> (ECDH) 的橢圓曲線 Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="5a12c-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="5a12c-138">秘密合約和金鑰交換</span><span class="sxs-lookup"><span data-stu-id="5a12c-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="5a12c-139">P256、P384、P521</span><span class="sxs-lookup"><span data-stu-id="5a12c-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5a12c-140"> (ECDSA) 的橢圓曲線數位簽章演算法</span><span class="sxs-lookup"><span data-stu-id="5a12c-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="5a12c-141">簽章</span><span class="sxs-lookup"><span data-stu-id="5a12c-141">Signatures</span></span>                        | <span data-ttu-id="5a12c-142">P256、P384、P521</span><span class="sxs-lookup"><span data-stu-id="5a12c-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5a12c-143">RSA</span><span class="sxs-lookup"><span data-stu-id="5a12c-143">RSA</span></span>                                                | <span data-ttu-id="5a12c-144">非對稱式加密和簽署</span><span class="sxs-lookup"><span data-stu-id="5a12c-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="5a12c-145">512至16384以64位遞增</span><span class="sxs-lookup"><span data-stu-id="5a12c-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5a12c-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a12c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a12c-147">**CNG 演算法識別碼**</span><span class="sxs-lookup"><span data-stu-id="5a12c-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="5a12c-148">CNG 金鑰儲存功能</span><span class="sxs-lookup"><span data-stu-id="5a12c-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="5a12c-149">瞭解密碼編譯提供者</span><span class="sxs-lookup"><span data-stu-id="5a12c-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
