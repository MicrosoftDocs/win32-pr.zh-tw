---
description: Windows Installer 允許每個內容安裝一個產品程式碼的實例，而且兩個可能的內容類型如下： MachineUser 如果產品代碼保持不變，則只有一個實例可以安裝在電腦內容中，而且每個使用者內容只能安裝一個實例。 多個實例必須具有不同的產品代碼，且無法共用檔案資料或非資料，才能保持隔離。 Windows Installer 無法使用並行安裝來安裝多個產品實例。 但是，如果您針對產品或修補程式的每個實例都有個別的安裝套件，就可以安裝多個產品的實例。 然後每個封裝都可以保留自己的資料集，並擁有自己的唯一產品代碼。 從執行 Windows Server 2003 和 Windows XP Service Pack 1 (SP1) 的安裝程式開始，您可以使用產品程式碼轉換和一個 .msi 封裝或一個修補程式，安裝多個產品的實例。 您也可以使用產品程式碼轉換，以 Windows 2000 （含 Service Pack 4） (SP4) 和 Windows Installer&160）來安裝多個產品的實例 \# 。3.0。 使用舊版安裝程式來安裝多個產品實例的唯一方式，就是針對每個實例都有個別的安裝套件。 使用實例轉換可大幅減少支援產品之多個實例所需的工作。 您可以為產品撰寫一個基底 Windows Installer 套件，然後針對每個實例的多個實例轉換，變更產品程式碼和管理資料。如需詳細資訊，請參閱使用實例轉換撰寫多個實例，以及使用實例轉換來安裝多個實例。
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: 安裝多個產品和修補程式實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3a1de5de7cc63d5eed2e191d77915630761561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194749"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a><span data-ttu-id="3c756-112">安裝多個產品和修補程式實例</span><span class="sxs-lookup"><span data-stu-id="3c756-112">Installing Multiple Instances of Products and Patches</span></span>

<span data-ttu-id="3c756-113">Windows Installer 允許每個內容安裝一個產品程式碼的實例，而這兩種可能的內容類型如下：</span><span class="sxs-lookup"><span data-stu-id="3c756-113">Windows Installer permits one instance of a product code to be installed per context, and the two possible types of context are the following:</span></span>

-   <span data-ttu-id="3c756-114">電腦</span><span class="sxs-lookup"><span data-stu-id="3c756-114">Machine</span></span>
-   <span data-ttu-id="3c756-115">User</span><span class="sxs-lookup"><span data-stu-id="3c756-115">User</span></span>

<span data-ttu-id="3c756-116">如果產品代碼保持不變，則只有一個實例可以安裝在電腦內容中，而且每個使用者內容只能安裝一個實例。</span><span class="sxs-lookup"><span data-stu-id="3c756-116">If a product code remains unchanged, only one instance can be installed in the machine context and only one instance can be installed in each user context.</span></span>

<span data-ttu-id="3c756-117">多個實例必須具有不同的產品代碼，且無法共用檔案資料或非資料，才能保持隔離。</span><span class="sxs-lookup"><span data-stu-id="3c756-117">For multiple instances to remain isolated, they must have different product codes and cannot share file data or nonfile data.</span></span> <span data-ttu-id="3c756-118">Windows Installer 無法使用 [並行安裝](concurrent-installations.md)來安裝多個產品實例。</span><span class="sxs-lookup"><span data-stu-id="3c756-118">The Windows Installer cannot install multiple instances of products using [concurrent installations](concurrent-installations.md).</span></span> <span data-ttu-id="3c756-119">但是，如果您針對產品或修補程式的每個實例都有個別的安裝套件，就可以安裝多個產品的實例。</span><span class="sxs-lookup"><span data-stu-id="3c756-119">However, you can install multiple instances of a product if you have a separate installation package for each instance of a product or patch.</span></span> <span data-ttu-id="3c756-120">然後每個封裝都可以保留自己的資料集，並擁有自己的唯一產品代碼。</span><span class="sxs-lookup"><span data-stu-id="3c756-120">Then each package can keep its own set of data and have its own unique product code.</span></span>

<span data-ttu-id="3c756-121">從執行 Windows Server 2003 和 Windows XP Service Pack 1 (SP1) 的安裝程式開始，您可以使用產品程式碼轉換和一個 .msi 封裝或一個修補程式，安裝多個產品的實例。</span><span class="sxs-lookup"><span data-stu-id="3c756-121">Starting with the installer running Windows Server 2003 and Windows XP with Service Pack 1 (SP1), you can install multiple instances of a product by using product code transforms and one .msi package or one patch.</span></span> <span data-ttu-id="3c756-122">您也可以使用產品程式碼轉換，以 Windows 2000 （含 Service Pack 4） (SP4) 和 Windows Installer 3.0 來安裝多個產品的實例。</span><span class="sxs-lookup"><span data-stu-id="3c756-122">You can also use product code transforms to install multiple instances of a product with Windows 2000 with Service Pack 4 (SP4) and Windows Installer  3.0.</span></span> <span data-ttu-id="3c756-123">使用舊版安裝程式來安裝多個產品實例的唯一方式，就是針對每個實例都有個別的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="3c756-123">The only way to install more than one instance of a product with previous versions of the installer is to have a separate installation package for each instance.</span></span>

<span data-ttu-id="3c756-124">使用實例轉換可大幅減少支援產品之多個實例所需的工作。</span><span class="sxs-lookup"><span data-stu-id="3c756-124">Using instance transforms significantly reduces the effort needed to support multiple instances of a product.</span></span> <span data-ttu-id="3c756-125">您可以為產品撰寫一個基底 Windows Installer 套件，然後針對每個實例的多個實例轉換，變更產品程式碼和管理資料。</span><span class="sxs-lookup"><span data-stu-id="3c756-125">You can author one base Windows Installer package for a product and then multiple instance transforms that change the product code and manage data for each instance.</span></span>

<span data-ttu-id="3c756-126">如需詳細資訊，請參閱使用實例 [轉換撰寫多個實例](authoring-multiple-instances-with-instance-transforms.md) ，以及 [使用實例轉換來安裝多個](installing-multiple-instances-with-instance-transforms.md)實例。</span><span class="sxs-lookup"><span data-stu-id="3c756-126">For more information, see [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md) and [Installing Multiple Instances with Instance Transforms](installing-multiple-instances-with-instance-transforms.md).</span></span>

 

 



