---
description: 密碼編譯 API：新一代 (CNG) 定義下列用來執行 CNG 金鑰儲存作業的功能。
ms.assetid: b0fb174b-75d7-4203-88ab-8469fa85f208
title: CNG 金鑰儲存功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c40a56fdff27b78d733421ad33a4c88289156cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689472"
---
# <a name="cng-key-storage-functions"></a><span data-ttu-id="e28ba-103">CNG 金鑰儲存功能</span><span class="sxs-lookup"><span data-stu-id="e28ba-103">CNG Key Storage Functions</span></span>

<span data-ttu-id="e28ba-104">密碼編譯 API：新一代 (CNG) 定義下列用來執行 CNG 金鑰儲存作業的功能。</span><span class="sxs-lookup"><span data-stu-id="e28ba-104">Cryptography API: Next Generation (CNG) defines the following functions which are used to perform CNG key storage operations.</span></span>

-   [<span data-ttu-id="e28ba-105">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-105">**NCryptCreatePersistedKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
-   [<span data-ttu-id="e28ba-106">**NCryptDecrypt**</span><span class="sxs-lookup"><span data-stu-id="e28ba-106">**NCryptDecrypt**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptdecrypt)
-   [<span data-ttu-id="e28ba-107">**NCryptDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-107">**NCryptDeleteKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptdeletekey)
-   [<span data-ttu-id="e28ba-108">**NCryptDeriveKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-108">**NCryptDeriveKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptderivekey)
-   [<span data-ttu-id="e28ba-109">**NCryptEncrypt**</span><span class="sxs-lookup"><span data-stu-id="e28ba-109">**NCryptEncrypt**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptencrypt)
-   [<span data-ttu-id="e28ba-110">**NCryptEnumAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="e28ba-110">**NCryptEnumAlgorithms**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptenumalgorithms)
-   [<span data-ttu-id="e28ba-111">**NCryptEnumKeys**</span><span class="sxs-lookup"><span data-stu-id="e28ba-111">**NCryptEnumKeys**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptenumkeys)
-   [<span data-ttu-id="e28ba-112">**NCryptEnumStorageProviders**</span><span class="sxs-lookup"><span data-stu-id="e28ba-112">**NCryptEnumStorageProviders**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptenumstorageproviders)
-   [<span data-ttu-id="e28ba-113">**NCryptExportKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-113">**NCryptExportKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptexportkey)
-   [<span data-ttu-id="e28ba-114">**NCryptFinalizeKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-114">**NCryptFinalizeKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey)
-   [<span data-ttu-id="e28ba-115">**NCryptFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="e28ba-115">**NCryptFreeBuffer**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreebuffer)
-   [<span data-ttu-id="e28ba-116">**NCryptFreeObject**</span><span class="sxs-lookup"><span data-stu-id="e28ba-116">**NCryptFreeObject**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject)
-   [<span data-ttu-id="e28ba-117">**NCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="e28ba-117">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
-   [<span data-ttu-id="e28ba-118">**NCryptImportKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-118">**NCryptImportKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey)
-   [<span data-ttu-id="e28ba-119">**NCryptIsAlgSupported**</span><span class="sxs-lookup"><span data-stu-id="e28ba-119">**NCryptIsAlgSupported**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptisalgsupported)
-   [<span data-ttu-id="e28ba-120">**NCryptIsKeyHandle**</span><span class="sxs-lookup"><span data-stu-id="e28ba-120">**NCryptIsKeyHandle**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptiskeyhandle)
-   [<span data-ttu-id="e28ba-121">**NCryptNotifyChangeKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-121">**NCryptNotifyChangeKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptnotifychangekey)
-   [<span data-ttu-id="e28ba-122">**NCryptOpenKey**</span><span class="sxs-lookup"><span data-stu-id="e28ba-122">**NCryptOpenKey**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey)
-   [<span data-ttu-id="e28ba-123">**NCryptOpenStorageProvider**</span><span class="sxs-lookup"><span data-stu-id="e28ba-123">**NCryptOpenStorageProvider**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenstorageprovider)
-   [<span data-ttu-id="e28ba-124">**NCryptSecretAgreement**</span><span class="sxs-lookup"><span data-stu-id="e28ba-124">**NCryptSecretAgreement**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsecretagreement)
-   [<span data-ttu-id="e28ba-125">**NCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="e28ba-125">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
-   [<span data-ttu-id="e28ba-126">**NCryptSignHash**</span><span class="sxs-lookup"><span data-stu-id="e28ba-126">**NCryptSignHash**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash)
-   [<span data-ttu-id="e28ba-127">**NCryptTranslateHandle**</span><span class="sxs-lookup"><span data-stu-id="e28ba-127">**NCryptTranslateHandle**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncrypttranslatehandle)
-   [<span data-ttu-id="e28ba-128">**NCryptVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="e28ba-128">**NCryptVerifySignature**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature)

 

 



