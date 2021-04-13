---
description: 深入瞭解： CNG SSL 提供者函式
ms.assetid: dd1313c7-e0b1-41e6-b82e-a66fc26b4ac0
title: CNG SSL 提供者函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c433e99131b63e995453d506002383e883bf99b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510962"
---
# <a name="cng-ssl-provider-functions"></a><span data-ttu-id="d2b09-103">CNG SSL 提供者函式</span><span class="sxs-lookup"><span data-stu-id="d2b09-103">CNG SSL Provider Functions</span></span>

<span data-ttu-id="d2b09-104">CNG 提供了或與 CNG SSL 提供者一起使用的下列功能：</span><span class="sxs-lookup"><span data-stu-id="d2b09-104">CNG provides the following functions that are used by or with a CNG SSL provider:</span></span>

-   [<span data-ttu-id="d2b09-105">**SslChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="d2b09-105">**SslChangeNotify**</span></span>](sslchangenotify.md)
-   [<span data-ttu-id="d2b09-106">**SslComputeClientAuthHash**</span><span class="sxs-lookup"><span data-stu-id="d2b09-106">**SslComputeClientAuthHash**</span></span>](sslcomputeclientauthhash.md)
-   [<span data-ttu-id="d2b09-107">**SslComputeEapKeyBlock**</span><span class="sxs-lookup"><span data-stu-id="d2b09-107">**SslComputeEapKeyBlock**</span></span>](sslcomputeeapkeyblock.md)
-   [<span data-ttu-id="d2b09-108">**SslComputeFinishedHash**</span><span class="sxs-lookup"><span data-stu-id="d2b09-108">**SslComputeFinishedHash**</span></span>](sslcomputefinishedhash.md)
-   [<span data-ttu-id="d2b09-109">**SslCreateClientAuthHash**</span><span class="sxs-lookup"><span data-stu-id="d2b09-109">**SslCreateClientAuthHash**</span></span>](sslcreateclientauthhash.md)
-   [<span data-ttu-id="d2b09-110">**SslCreateEphemeralKey**</span><span class="sxs-lookup"><span data-stu-id="d2b09-110">**SslCreateEphemeralKey**</span></span>](sslcreateephemeralkey.md)
-   [<span data-ttu-id="d2b09-111">**SslCreateHandshakeHash**</span><span class="sxs-lookup"><span data-stu-id="d2b09-111">**SslCreateHandshakeHash**</span></span>](sslcreatehandshakehash.md)
-   [<span data-ttu-id="d2b09-112">**SslDecrementProviderReferenceCount**</span><span class="sxs-lookup"><span data-stu-id="d2b09-112">**SslDecrementProviderReferenceCount**</span></span>](ssldecrementproviderreferencecount.md)
-   [<span data-ttu-id="d2b09-113">**SslDecryptPacket**</span><span class="sxs-lookup"><span data-stu-id="d2b09-113">**SslDecryptPacket**</span></span>](ssldecryptpacket.md)
-   [<span data-ttu-id="d2b09-114">**SslEncryptPacket**</span><span class="sxs-lookup"><span data-stu-id="d2b09-114">**SslEncryptPacket**</span></span>](sslencryptpacket.md)
-   [<span data-ttu-id="d2b09-115">**SslEnumCipherSuites**</span><span class="sxs-lookup"><span data-stu-id="d2b09-115">**SslEnumCipherSuites**</span></span>](sslenumciphersuites.md)
-   [<span data-ttu-id="d2b09-116">**SslEnumProtocolProviders**</span><span class="sxs-lookup"><span data-stu-id="d2b09-116">**SslEnumProtocolProviders**</span></span>](sslenumprotocolproviders.md)
-   [<span data-ttu-id="d2b09-117">**SslExportKey**</span><span class="sxs-lookup"><span data-stu-id="d2b09-117">**SslExportKey**</span></span>](sslexportkey.md)
-   [<span data-ttu-id="d2b09-118">**SslExportKeyingMaterial**</span><span class="sxs-lookup"><span data-stu-id="d2b09-118">**SslExportKeyingMaterial**</span></span>](sslexportkeyingmaterial.md)
-   [<span data-ttu-id="d2b09-119">**SslFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="d2b09-119">**SslFreeBuffer**</span></span>](sslfreebuffer.md)
-   [<span data-ttu-id="d2b09-120">**SslFreeObject**</span><span class="sxs-lookup"><span data-stu-id="d2b09-120">**SslFreeObject**</span></span>](sslfreeobject.md)
-   [<span data-ttu-id="d2b09-121">**SslGenerateMasterKey**</span><span class="sxs-lookup"><span data-stu-id="d2b09-121">**SslGenerateMasterKey**</span></span>](sslgeneratemasterkey.md)
-   [<span data-ttu-id="d2b09-122">**SslGenerateSessionKeys**</span><span class="sxs-lookup"><span data-stu-id="d2b09-122">**SslGenerateSessionKeys**</span></span>](sslgeneratesessionkeys.md)
-   [<span data-ttu-id="d2b09-123">**SslGetCipherSuitePRFHashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="d2b09-123">**SslGetCipherSuitePRFHashAlgorithm**</span></span>](sslgetciphersuiteprfhashalgorithm.md)
-   [<span data-ttu-id="d2b09-124">**SslGetKeyProperty**</span><span class="sxs-lookup"><span data-stu-id="d2b09-124">**SslGetKeyProperty**</span></span>](sslgetkeyproperty.md)
-   [<span data-ttu-id="d2b09-125">**SslGetProviderProperty**</span><span class="sxs-lookup"><span data-stu-id="d2b09-125">**SslGetProviderProperty**</span></span>](sslgetproviderproperty.md)
-   [<span data-ttu-id="d2b09-126">**SslHashHandshake**</span><span class="sxs-lookup"><span data-stu-id="d2b09-126">**SslHashHandshake**</span></span>](sslhashhandshake.md)
-   [<span data-ttu-id="d2b09-127">**SslImportKey**</span><span class="sxs-lookup"><span data-stu-id="d2b09-127">**SslImportKey**</span></span>](sslimportkey.md)
-   [<span data-ttu-id="d2b09-128">**SslImportMasterKey**</span><span class="sxs-lookup"><span data-stu-id="d2b09-128">**SslImportMasterKey**</span></span>](sslimportmasterkey.md)
-   [<span data-ttu-id="d2b09-129">**SslIncrementProviderReferenceCount**</span><span class="sxs-lookup"><span data-stu-id="d2b09-129">**SslIncrementProviderReferenceCount**</span></span>](sslincrementproviderreferencecount.md)
-   [<span data-ttu-id="d2b09-130">**SslLookupCipherLengths**</span><span class="sxs-lookup"><span data-stu-id="d2b09-130">**SslLookupCipherLengths**</span></span>](ssllookupcipherlengths.md)
-   [<span data-ttu-id="d2b09-131">**SslLookupCipherSuiteInfo**</span><span class="sxs-lookup"><span data-stu-id="d2b09-131">**SslLookupCipherSuiteInfo**</span></span>](ssllookupciphersuiteinfo.md)
-   [<span data-ttu-id="d2b09-132">**SslOpenPrivateKey**</span><span class="sxs-lookup"><span data-stu-id="d2b09-132">**SslOpenPrivateKey**</span></span>](sslopenprivatekey.md)
-   [<span data-ttu-id="d2b09-133">**SslOpenProvider**</span><span class="sxs-lookup"><span data-stu-id="d2b09-133">**SslOpenProvider**</span></span>](sslopenprovider.md)
-   [<span data-ttu-id="d2b09-134">**SslSignHash**</span><span class="sxs-lookup"><span data-stu-id="d2b09-134">**SslSignHash**</span></span>](sslsignhash.md)
-   [<span data-ttu-id="d2b09-135">**SslVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="d2b09-135">**SslVerifySignature**</span></span>](sslverifysignature.md)

 

 



