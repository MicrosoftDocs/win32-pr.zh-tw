---
description: 類別提供者會管理 WMI 的類別或一系列的類別。
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: 撰寫類別提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986973"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="dbf5b-103">撰寫類別提供者</span><span class="sxs-lookup"><span data-stu-id="dbf5b-103">Writing a Class Provider</span></span>

<span data-ttu-id="dbf5b-104">類別提供者會管理 WMI 的類別或一系列的類別。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="dbf5b-105">類別提供者可以是 push 或 pull;也就是說，它可以儲存本身的資料，或允許 WMI 將其資料儲存在 Windows 管理服務中。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="dbf5b-106">雖然類別提供者是安裝在特定的電腦上，但它可以變更整個企業的類別定義。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="dbf5b-107">因此，大部分的開發人員通常不會建立類別提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="dbf5b-108">在建立類別提供者之前，請確認支援的類別確實必須動態產生。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="dbf5b-109">在大多數情況下，類別的清單會變得緩慢且有限。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="dbf5b-110">如果是這種情況，您就不需要建立類別提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="dbf5b-111">相反地，您可以使用 WMI API 或 MOF 檔案，將您的類別定義放在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="dbf5b-112">下列程式描述如何執行類別提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="dbf5b-113">**若要執行類別提供者**</span><span class="sxs-lookup"><span data-stu-id="dbf5b-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="dbf5b-114">判斷您的提供者是否為 push 或 pull 提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="dbf5b-115">提取提供者會動態提供資料以回應應用程式要求，而推送提供者則會在 WMI 儲存機制中儲存一次資料。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="dbf5b-116">如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="dbf5b-117">使用 WMI 設計和註冊您的類別提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="dbf5b-118">類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)實例，向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="dbf5b-119">如需詳細資訊，請參閱 [註冊類別提供者](registering-a-class-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="dbf5b-120">為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="dbf5b-121">WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="dbf5b-122">如果您要設計推播提供者， **IWbemProviderInit** 是您將會執行的唯一介面。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="dbf5b-123">如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="dbf5b-124">強烈建議您使用類別提供者來使用多執行緒模型「兩者」。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="dbf5b-125">加入提供者所需的任何其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="dbf5b-126">設計您的提供者時，您很可能需要呼叫 WMI 介面。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="dbf5b-127">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [維護提供者中的安全性層級](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="dbf5b-128">取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="dbf5b-129">如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="dbf5b-130">為您的提供者執行 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="dbf5b-131">[**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面是提取類別提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="dbf5b-132">如需詳細資訊，請參閱 [執行類別提供者的主要介面](implementing-the-primary-interface-for-a-class-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="dbf5b-133">以您的新程式碼取代預先存在的提供者。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="dbf5b-134">如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="dbf5b-135">如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf5b-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



