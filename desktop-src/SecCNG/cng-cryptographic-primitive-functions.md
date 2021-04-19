---
description: 密碼編譯 API：新一代 (CNG) 定義下列用來執行密碼編譯作業的功能。
ms.assetid: 7200efb5-2893-476c-9ad0-ba49bce92387
title: CNG 密碼編譯基本函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e173d9d92a3722352052bbe973cadf0b2bb762e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986287"
---
# <a name="cng-cryptographic-primitive-functions"></a><span data-ttu-id="b789c-103">CNG 密碼編譯基本函數</span><span class="sxs-lookup"><span data-stu-id="b789c-103">CNG Cryptographic Primitive Functions</span></span>

<span data-ttu-id="b789c-104">密碼編譯 API：新一代 (CNG) 定義下列用來執行密碼編譯作業的功能。</span><span class="sxs-lookup"><span data-stu-id="b789c-104">Cryptography API: Next Generation (CNG) defines the following functions that are used for performing cryptographic operations.</span></span>

-   [<span data-ttu-id="b789c-105">**BCryptCloseAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="b789c-105">**BCryptCloseAlgorithmProvider**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider)
-   [<span data-ttu-id="b789c-106">**BCryptCreateHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-106">**BCryptCreateHash**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)
-   [<span data-ttu-id="b789c-107">**BCryptCreateMultiHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-107">**BCryptCreateMultiHash**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash)
-   [<span data-ttu-id="b789c-108">**BCryptDecrypt**</span><span class="sxs-lookup"><span data-stu-id="b789c-108">**BCryptDecrypt**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)
-   [<span data-ttu-id="b789c-109">**BCryptDeriveKey**</span><span class="sxs-lookup"><span data-stu-id="b789c-109">**BCryptDeriveKey**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptderivekey)
-   [<span data-ttu-id="b789c-110">**BCryptDestroyHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-110">**BCryptDestroyHash**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash)
-   [<span data-ttu-id="b789c-111">**BCryptDestroyKey**</span><span class="sxs-lookup"><span data-stu-id="b789c-111">**BCryptDestroyKey**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroykey)
-   [<span data-ttu-id="b789c-112">**BCryptDestroySecret**</span><span class="sxs-lookup"><span data-stu-id="b789c-112">**BCryptDestroySecret**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroysecret)
-   [<span data-ttu-id="b789c-113">**BCryptDuplicateHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-113">**BCryptDuplicateHash**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash)
-   [<span data-ttu-id="b789c-114">**BCryptDuplicateKey**</span><span class="sxs-lookup"><span data-stu-id="b789c-114">**BCryptDuplicateKey**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatekey)
-   [<span data-ttu-id="b789c-115">**BCryptEncrypt**</span><span class="sxs-lookup"><span data-stu-id="b789c-115">**BCryptEncrypt**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt)
-   [<span data-ttu-id="b789c-116">**BCryptExportKey**</span><span class="sxs-lookup"><span data-stu-id="b789c-116">**BCryptExportKey**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey)
-   [<span data-ttu-id="b789c-117">**BCryptFinalizeKeyPair**</span><span class="sxs-lookup"><span data-stu-id="b789c-117">**BCryptFinalizeKeyPair**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinalizekeypair)
-   [<span data-ttu-id="b789c-118">**BCryptFinishHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-118">**BCryptFinishHash**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash)
-   [<span data-ttu-id="b789c-119">**BCryptFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="b789c-119">**BCryptFreeBuffer**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer)
-   [<span data-ttu-id="b789c-120">**BCryptGenerateKeyPair**</span><span class="sxs-lookup"><span data-stu-id="b789c-120">**BCryptGenerateKeyPair**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)
-   [<span data-ttu-id="b789c-121">**BCryptGenerateSymmetricKey**</span><span class="sxs-lookup"><span data-stu-id="b789c-121">**BCryptGenerateSymmetricKey**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey)
-   [<span data-ttu-id="b789c-122">**BCryptGenRandom**</span><span class="sxs-lookup"><span data-stu-id="b789c-122">**BCryptGenRandom**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom)
-   [<span data-ttu-id="b789c-123">**BCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="b789c-123">**BCryptGetProperty**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty)
-   [<span data-ttu-id="b789c-124">**BCryptHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-124">**BCryptHash**</span></span>](/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthash)
-   [<span data-ttu-id="b789c-125">**BCryptHashData**</span><span class="sxs-lookup"><span data-stu-id="b789c-125">**BCryptHashData**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata)
-   [<span data-ttu-id="b789c-126">**BCryptImportKey**</span><span class="sxs-lookup"><span data-stu-id="b789c-126">**BCryptImportKey**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey)
-   [<span data-ttu-id="b789c-127">**BCryptImportKeyPair**</span><span class="sxs-lookup"><span data-stu-id="b789c-127">**BCryptImportKeyPair**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair)
-   [<span data-ttu-id="b789c-128">**BCryptKeyDerivation**</span><span class="sxs-lookup"><span data-stu-id="b789c-128">**BCryptKeyDerivation**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation)
-   [<span data-ttu-id="b789c-129">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="b789c-129">**BCryptOpenAlgorithmProvider**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
-   [<span data-ttu-id="b789c-130">**BCryptProcessMultiOperations**</span><span class="sxs-lookup"><span data-stu-id="b789c-130">**BCryptProcessMultiOperations**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptprocessmultioperations)
-   [<span data-ttu-id="b789c-131">**BCryptSecretAgreement**</span><span class="sxs-lookup"><span data-stu-id="b789c-131">**BCryptSecretAgreement**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsecretagreement)
-   [<span data-ttu-id="b789c-132">**BCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="b789c-132">**BCryptSetProperty**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty)
-   [<span data-ttu-id="b789c-133">**BCryptSignHash**</span><span class="sxs-lookup"><span data-stu-id="b789c-133">**BCryptSignHash**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash)
-   [<span data-ttu-id="b789c-134">**BCryptVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="b789c-134">**BCryptVerifySignature**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature)

 

 



