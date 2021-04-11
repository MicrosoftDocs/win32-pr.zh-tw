---
description: MUI 的優點說明
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: MUI 的優點說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1915e58e28ac9c7b3a43cc0ba217b8d56657c1b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026181"
---
# <a name="benefits-of-mui-explained"></a><span data-ttu-id="7865f-103">MUI 的優點說明</span><span class="sxs-lookup"><span data-stu-id="7865f-103">Benefits of MUI Explained</span></span>

-   [<span data-ttu-id="7865f-104">適用于開發人員的 MUI 權益</span><span class="sxs-lookup"><span data-stu-id="7865f-104">MUI benefits for developers</span></span>](#mui-benefits-for-developers)
-   [<span data-ttu-id="7865f-105">企業適用的 MUI 權益</span><span class="sxs-lookup"><span data-stu-id="7865f-105">MUI benefits for enterprises</span></span>](#mui-benefits-for-enterprises)
-   [<span data-ttu-id="7865f-106">適用于 Oem 的 MUI 權益</span><span class="sxs-lookup"><span data-stu-id="7865f-106">MUI benefits for OEMs</span></span>](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a><span data-ttu-id="7865f-107">適用于開發人員的 MUI 權益</span><span class="sxs-lookup"><span data-stu-id="7865f-107">MUI benefits for developers</span></span>

<span data-ttu-id="7865f-108">有許多可能的方法可以在應用程式中執行 MUI 解決方案，但每個可能性都是三種基本方法之一的變化：</span><span class="sxs-lookup"><span data-stu-id="7865f-108">There are many possible ways to implement a MUI solution in applications, but each possibility is a variation of one of three basic methods:</span></span>

1.  <span data-ttu-id="7865f-109">使用內建資源編譯一個二進位 (，) 適用于每種語言。</span><span class="sxs-lookup"><span data-stu-id="7865f-109">Compiling one binary (with built-in resources) for each language.</span></span> <span data-ttu-id="7865f-110">這是繼承應用程式的 *事實上* 標準，因為這是標準開發工具（例如 Microsoft Visual Studio）所支援的主要模型。</span><span class="sxs-lookup"><span data-stu-id="7865f-110">This is the *de facto* standard for legacy applications, as this is the primary model supported by standard development tools such as Microsoft Visual Studio.</span></span> <span data-ttu-id="7865f-111">此模型確實需要多個語言的多個二進位檔，並在單一映射部署和多語言案例方面有一些限制。</span><span class="sxs-lookup"><span data-stu-id="7865f-111">This model does require multiple binaries for multiple languages and has limitations with regards to single image deployment and multi-lingual scenarios.</span></span> <span data-ttu-id="7865f-112">請注意，使用此模型開發的應用程式將繼續在 Windows Vista 上運作，而提供的工具可協助開發人員從這個模型移到第三種方法中所述的現代化模型。</span><span class="sxs-lookup"><span data-stu-id="7865f-112">It should be noted that applications developed with this model will continue to work on Windows Vista, and that tools are provided that help developers move from this model to the more modern model outlined in the third method.</span></span>
2.  <span data-ttu-id="7865f-113">具有一個語言中立的核心二進位檔，其中有一個多語言資源動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="7865f-113">Having one language-neutral core binary with one multi-language resource dynamic-link library (DLL).</span></span> <span data-ttu-id="7865f-114">這種模型肯定是方便 MUI，但很難更新資源二進位檔以容納新的語言。</span><span class="sxs-lookup"><span data-stu-id="7865f-114">This model is definitely MUI-friendly but makes it difficult to update the resource binaries to accommodate new languages.</span></span> <span data-ttu-id="7865f-115">假設除了英文、法文和日文之外，您也想要支援德文。</span><span class="sxs-lookup"><span data-stu-id="7865f-115">Suppose that besides English, French and Japanese, you want to also support German.</span></span> <span data-ttu-id="7865f-116">您必須提供整個新的資源二進位檔，並將其部署給可能不需要德文的使用者。</span><span class="sxs-lookup"><span data-stu-id="7865f-116">A whole new resource binary would need to be provided and deployed to your users who may not necessarily need German.</span></span>
3.  <span data-ttu-id="7865f-117">具有一個語言中立的核心二進位檔，每種語言都有一組資源 Dll。</span><span class="sxs-lookup"><span data-stu-id="7865f-117">Having one language-neutral core binary with one set of resource DLLs per language.</span></span> <span data-ttu-id="7865f-118">這是作業系統本身在 Windows Vista 中的執行方式，而開發人員則建議將此模型用於應用程式，因為它提供的是上述兩個模型。</span><span class="sxs-lookup"><span data-stu-id="7865f-118">This is the way the operating system itself is implemented in Windows Vista, and developers are encouraged to use this model for applications as it offers more than the previous two models.</span></span>

<span data-ttu-id="7865f-119">在 Windows Vista 發行之前，缺乏此第二個模型的內建支援，使其難以採用。</span><span class="sxs-lookup"><span data-stu-id="7865f-119">Prior to the Windows Vista release, the lack of built-in support for this latter model made it hard to adopt.</span></span> <span data-ttu-id="7865f-120">不過，這已經改變，而此模型的優點很多，因此成為應用程式的絕佳模型：</span><span class="sxs-lookup"><span data-stu-id="7865f-120">However, this has changed, and the benefits of this model are numerous and make it a great model for your applications:</span></span>

-   <span data-ttu-id="7865f-121">您可以使用與 Windows Vista 相同的方式，讓應用程式進行多語言的行為，並為使用者提供一致的顯示語言體驗。</span><span class="sxs-lookup"><span data-stu-id="7865f-121">Applications can be made multi-lingual and can behave in the same way as Windows Vista, providing a consistent display language experience for users.</span></span>
-   <span data-ttu-id="7865f-122">在發行應用程式的其他語言時，會增加彈性。</span><span class="sxs-lookup"><span data-stu-id="7865f-122">Flexibility is increased in releasing additional languages for an application.</span></span> <span data-ttu-id="7865f-123">其他語言可以與核心程式代碼分開發行，這表示您可以視需要在一段時間內加入新語言的支援。</span><span class="sxs-lookup"><span data-stu-id="7865f-123">Additional languages can be released independently of the core code, which means that support for new languages can be added over time as needed.</span></span>
-   <span data-ttu-id="7865f-124">在建立和維護更多語言版本時，會降低成本。</span><span class="sxs-lookup"><span data-stu-id="7865f-124">Cost is reduced in creating and servicing more language releases.</span></span>
-   <span data-ttu-id="7865f-125">Oem 和企業可以輕鬆地將應用程式整合到他們的全球化電腦影像中，以便寄送至不同的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="7865f-125">OEMs and enterprises can easily integrate applications into their globalized PC image—ready for shipment to different countries.</span></span>
-   <span data-ttu-id="7865f-126">提供可協助您將應用程式遷移至 Windows Vista MUI 模型的工具和指導方針。</span><span class="sxs-lookup"><span data-stu-id="7865f-126">Tools and guidelines that help you migrate your application to the Windows Vista MUI model are available.</span></span> <span data-ttu-id="7865f-127">特別是，MSDN 在 MUI 上提供一 [組重要的檔集](multilingual-user-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="7865f-127">In particular, MSDN provides a [significant set of documentation](multilingual-user-interface.md) on MUI.</span></span>

## <a name="mui-benefits-for-enterprises"></a><span data-ttu-id="7865f-128">企業適用的 MUI 權益</span><span class="sxs-lookup"><span data-stu-id="7865f-128">MUI benefits for enterprises</span></span>

<span data-ttu-id="7865f-129">MUI 為企業提供兩大優點：</span><span class="sxs-lookup"><span data-stu-id="7865f-129">MUI offers two major benefits for enterprises:</span></span>

-   <span data-ttu-id="7865f-130">單一映射安裝： MUI 可讓企業使用單一安裝來推出、支援及維護相同的全球 (或) 映射的任何部分。</span><span class="sxs-lookup"><span data-stu-id="7865f-130">Single image installation: MUI allows enterprises to roll out, support and maintain the same worldwide (or any part thereof) image with a single installation.</span></span> <span data-ttu-id="7865f-131">Windows Vista 擴充了作業系統的單一映射推出，因此商務應用程式也可以部署為相同映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="7865f-131">Windows Vista extends the single-image rollout of the operating system, so that business applications can also be deployed as part of the same image.</span></span>
-   <span data-ttu-id="7865f-132">多語系桌面的支援：多個當地語系化的 UI 語言套件可以安裝在桌面上，讓多個使用者可以共用單一桌面，同時仍使用自己慣用的 UI 語言。</span><span class="sxs-lookup"><span data-stu-id="7865f-132">Support for multilingual desktops: Multiple localized UI language packs can be installed on a desktop, which enables multiple users to share a single desktop while still using their own preferred UI languages.</span></span> <span data-ttu-id="7865f-133">這也適用于需要對所有正式語音 (語言進行同等處理的公用電腦，例如在加拿大和歐盟) ，以及將電腦用於漫遊使用者的情況下。</span><span class="sxs-lookup"><span data-stu-id="7865f-133">This also applies to public computers, which need equal treatment for all the officially spoken languages (such as might be the case in Canada and in the European Union), and to shared computers for roaming users.</span></span>

## <a name="mui-benefits-for-oems"></a><span data-ttu-id="7865f-134">適用于 Oem 的 MUI 權益</span><span class="sxs-lookup"><span data-stu-id="7865f-134">MUI benefits for OEMs</span></span>

<span data-ttu-id="7865f-135">Oem 的主要優點是 MUI 啟用的單一映射安裝，因為它可讓您建立包含所有必要語言的映射，以便有效地將目標設為地理區域，以及將語言選擇延遲到使用者的初始安裝電腦上。</span><span class="sxs-lookup"><span data-stu-id="7865f-135">The major benefit for OEMs is the single image installation that MUI enables, as it makes it possible to create images that contain all necessary languages to target a geographic zone effectively, and to delay the language choice to the user's initial installation of the computer.</span></span> <span data-ttu-id="7865f-136">特別是，這可讓您更有效地管理 Oem 的清查。</span><span class="sxs-lookup"><span data-stu-id="7865f-136">In particular, this enables a more effective management of inventory for OEMs.</span></span>

<span data-ttu-id="7865f-137">藉由提供應用程式的 MUI 支援，Windows Vista 也可讓 Oem 在其映射上提供加值應用程式，同時從單一映射安裝獲益，只要這些應用程式已啟用 MUI 即可。</span><span class="sxs-lookup"><span data-stu-id="7865f-137">By providing MUI support for applications, Windows Vista also enables OEMs to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI enabled.</span></span>

 

 



