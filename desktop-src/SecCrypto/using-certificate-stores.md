---
description: CAPICOM 使用數位憑證來建立簽章、建立封包訊息時加密會話加密金鑰，以及在收到包訊息時將加密的工作階段金鑰解密。
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: 使用憑證存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682068ba8f2f88d0fedabeef7ccee676f092e52e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977182"
---
# <a name="using-certificate-stores"></a><span data-ttu-id="53809-103">使用憑證存放區</span><span class="sxs-lookup"><span data-stu-id="53809-103">Using Certificate Stores</span></span>

<span data-ttu-id="53809-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="53809-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="53809-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="53809-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="53809-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="53809-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="53809-107">CAPICOM 使用 [*數位憑證*](../secgloss/d-gly.md) 來建立簽章、建立封包訊息時加密會話加密金鑰，以及在收到包訊息時將加密的工作階段金鑰解密。</span><span class="sxs-lookup"><span data-stu-id="53809-107">CAPICOM uses [*digital certificates*](../secgloss/d-gly.md) to create signatures, encrypt session encryption keys when creating enveloped messages, and decrypt encrypted session keys when an enveloped message is received.</span></span> <span data-ttu-id="53809-108">根據預設，CAPICOM 會使用我存放區中的憑證，其具有相關聯的私密金鑰來建立 [*數位簽章*](../secgloss/d-gly.md) 和工作階段金鑰解密。</span><span class="sxs-lookup"><span data-stu-id="53809-108">By default, CAPICOM uses certificates in the My store that have an associated private key for both [*digital signatures*](../secgloss/d-gly.md) creation and session key decryption.</span></span> <span data-ttu-id="53809-109">在大多數情況下，應用程式永遠不需要開啟或直接處理憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="53809-109">In most cases, an application would never need to open or otherwise directly deal with a certificate store.</span></span>

<span data-ttu-id="53809-110">不過，建立封裝訊息的應用程式會使用每個預定的封包訊息收件者的 [*公開金鑰*](../secgloss/p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="53809-110">However, applications creating enveloped messages use the [*public key*](../secgloss/p-gly.md) of each intended recipient of an enveloped message.</span></span> <span data-ttu-id="53809-111">這些金鑰是取自預定收件者的憑證。</span><span class="sxs-lookup"><span data-stu-id="53809-111">These keys are retrieved from the certificates of the intended recipients.</span></span> <span data-ttu-id="53809-112">因此，若要建立一組預定收件者的封包訊息，則會在憑證存放區中收集這些收件者的憑證。</span><span class="sxs-lookup"><span data-stu-id="53809-112">Thus, to create enveloped messages for a group of intended recipients, the certificates of those recipients would be collected in a certificate store.</span></span>

<span data-ttu-id="53809-113">下表列出一般保存在使用者工作站上的標準憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="53809-113">The following table lists the standard certificate stores normally persisted on a user station.</span></span>



| <span data-ttu-id="53809-114">市集</span><span class="sxs-lookup"><span data-stu-id="53809-114">Store</span></span>        | <span data-ttu-id="53809-115">Description</span><span class="sxs-lookup"><span data-stu-id="53809-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53809-116">My</span><span class="sxs-lookup"><span data-stu-id="53809-116">My</span></span>           | <span data-ttu-id="53809-117">包含個人憑證。</span><span class="sxs-lookup"><span data-stu-id="53809-117">Contains personal certificates.</span></span> <span data-ttu-id="53809-118">這些憑證通常會有相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="53809-118">These certificates will usually have an associated private key.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="53809-119">其他人</span><span class="sxs-lookup"><span data-stu-id="53809-119">Other people</span></span> | <span data-ttu-id="53809-120">包含使用者通常會將封包訊息傳送至或從中接收簽署訊息的憑證。</span><span class="sxs-lookup"><span data-stu-id="53809-120">Contains the certificates of those that the user normally sends enveloped messages to or receives signed messages from.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="53809-121">Ca 和根目錄</span><span class="sxs-lookup"><span data-stu-id="53809-121">Ca and Root</span></span>  | <span data-ttu-id="53809-122">包含使用者 [*信任的證書*](../secgloss/r-gly.md) 頒發機構單位頒發證書給其他人的憑證。</span><span class="sxs-lookup"><span data-stu-id="53809-122">Contains the [*certificates*](../secgloss/r-gly.md) of certificate authorities that the user trusts to issue certificates to others.</span></span> <span data-ttu-id="53809-123">這些存放區中的憑證通常是由作業系統或使用者的網路系統管理員所提供。</span><span class="sxs-lookup"><span data-stu-id="53809-123">Certificates in these stores are normally supplied with the operating system or by the user's network administrator.</span></span> <span data-ttu-id="53809-124">根存放區中的憑證通常是自我簽署的。</span><span class="sxs-lookup"><span data-stu-id="53809-124">Certificates in the Root store are typically self-signed.</span></span> |



 

<span data-ttu-id="53809-125">您 \_ \_ 可以為字串提供不同的存放區名稱，以建立、開啟及保存其他的 CAPICOM 目前使用者存放區。</span><span class="sxs-lookup"><span data-stu-id="53809-125">Additional CAPICOM\_CURRENT\_USER stores can be created, opened, and persisted by giving a different store name as a string.</span></span> <span data-ttu-id="53809-126">如果該名稱的存放區不存在，就會建立並開啟空的存放區。</span><span class="sxs-lookup"><span data-stu-id="53809-126">If a store by that name does not exist, an empty store is created and opened.</span></span> <span data-ttu-id="53809-127">如果存放區存在，則會開啟該存放區，而且目前儲存在存放區中的任何憑證都可供使用。</span><span class="sxs-lookup"><span data-stu-id="53809-127">If a store does exist, it is opened and any certificates currently in the store are made available.</span></span>

<span data-ttu-id="53809-128">下列各節顯示憑證存放區工作的範例：</span><span class="sxs-lookup"><span data-stu-id="53809-128">The following sections show examples for certificate store tasks:</span></span>

-   [<span data-ttu-id="53809-129">開啟 Active Directory 儲存和正在抓取憑證</span><span class="sxs-lookup"><span data-stu-id="53809-129">Opening the Active Directory Store and Retrieving Certificates</span></span>](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [<span data-ttu-id="53809-130">將憑證新增至憑證存放區</span><span class="sxs-lookup"><span data-stu-id="53809-130">Adding Certificates to a Certificate Store</span></span>](adding-certificates-to-a-certificate-store.md)
-   [<span data-ttu-id="53809-131">使用不同位置的商店</span><span class="sxs-lookup"><span data-stu-id="53809-131">Using Stores in Different Locations</span></span>](using-stores-in-different-locations.md)
-   [<span data-ttu-id="53809-132">收集和驗證憑證</span><span class="sxs-lookup"><span data-stu-id="53809-132">Collecting and Verifying Certificates</span></span>](collecting-and-verifying-certificates.md)

 

 
