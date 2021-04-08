---
description: 使用 MakeCert 命令，利用 Internet Explorer 4.0 版或更新版本所提供的選項來建立測試憑證。
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: 使用 MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691400"
---
# <a name="using-makecert"></a><span data-ttu-id="ab69f-103">使用 MakeCert</span><span class="sxs-lookup"><span data-stu-id="ab69f-103">Using MakeCert</span></span>

<span data-ttu-id="ab69f-104">下列範例會使用 [MakeCert](makecert.md) 命令，利用 Internet Explorer 4.0 版或更新版本所提供的選項來建立測試憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="ab69f-105">建立由預設測試根目錄發出的憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="ab69f-106">將憑證儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="ab69f-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="ab69f-107">**MakeCert** *MyNew .cer*</span><span class="sxs-lookup"><span data-stu-id="ab69f-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="ab69f-108">建立由預設測試根目錄發出的憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="ab69f-109">將它儲存至憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="ab69f-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="ab69f-110">**MakeCert-ss** *MyNewStore*</span><span class="sxs-lookup"><span data-stu-id="ab69f-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="ab69f-111">建立由預設測試根目錄發出的憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="ab69f-112">建立金鑰容器，並將憑證儲存至存放區和檔案。</span><span class="sxs-lookup"><span data-stu-id="ab69f-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="ab69f-113">**MakeCert-sk** *MyNewKey* **-ss** *MyNewStore* *MyNew .cer*</span><span class="sxs-lookup"><span data-stu-id="ab69f-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="ab69f-114">建立由預設測試根目錄發出的憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="ab69f-115">建立私密金鑰檔案，並將憑證儲存至存放區和檔案。</span><span class="sxs-lookup"><span data-stu-id="ab69f-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="ab69f-116">**MakeCert-sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew .cer*</span><span class="sxs-lookup"><span data-stu-id="ab69f-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="ab69f-117">建立由預設測試根目錄發出的憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="ab69f-118">建立金鑰容器、將憑證儲存至存放區和檔案，然後將私密金鑰匯出。</span><span class="sxs-lookup"><span data-stu-id="ab69f-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="ab69f-119">**MakeCert-sk** *MyNewKey* **-ss** *MyNewStore* *MyNew .cer* **-pe**</span><span class="sxs-lookup"><span data-stu-id="ab69f-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="ab69f-120">使用預設的測試根目錄來建立憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="ab69f-121">將憑證儲存到存放區。</span><span class="sxs-lookup"><span data-stu-id="ab69f-121">Save the certificate to a store.</span></span> <span data-ttu-id="ab69f-122">然後讓新建立的憑證發出另一個憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="ab69f-123">將第二個憑證儲存至另一個存放區。</span><span class="sxs-lookup"><span data-stu-id="ab69f-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="ab69f-124">**MakeCert-sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert-是** *MyNewStore* **-ss** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="ab69f-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="ab69f-125">使用預設的測試根目錄來建立憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="ab69f-126">將憑證儲存至 [我的存放區]。</span><span class="sxs-lookup"><span data-stu-id="ab69f-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="ab69f-127">然後使用新建立的憑證建立另一個憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="ab69f-128">如果我的存放區中有一個以上的憑證，則必須使用其一般名稱來識別憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="ab69f-129">**MakeCert-sk** *MyNewKey* **-n "CN = XXZZYY"-ss my MakeCert-是 my in "XXZZYY"-ss** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="ab69f-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="ab69f-130">使用預設的測試根目錄來建立憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="ab69f-131">將憑證儲存到 MY store 和檔案。</span><span class="sxs-lookup"><span data-stu-id="ab69f-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="ab69f-132">然後使用新建立的 *MyNew* 憑證來建立另一個憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="ab69f-133">如果我的存放區中有一個以上的憑證，請使用憑證檔案名來唯一識別第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="ab69f-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="ab69f-134">**MakeCert-sk** *MyNewKey* **-n "CN = XXZZYY"-ss my** *MyNew .Cer* **MakeCert-是我的 ic** *MyNew .cer* **-ss** *AnotherStore*</span><span class="sxs-lookup"><span data-stu-id="ab69f-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



