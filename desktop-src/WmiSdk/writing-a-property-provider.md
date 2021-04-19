---
description: 屬性提供者會針對儲存在 WMI 儲存機制中之指定類別的實例，抓取和修改個別的屬性值。
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: 撰寫屬性提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988846"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="50637-103">撰寫屬性提供者</span><span class="sxs-lookup"><span data-stu-id="50637-103">Writing a Property Provider</span></span>

<span data-ttu-id="50637-104">屬性提供者會針對儲存在 WMI 儲存機制中之指定類別的實例，抓取和修改個別的屬性值。</span><span class="sxs-lookup"><span data-stu-id="50637-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="50637-105">下列程式描述如何建立屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="50637-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="50637-106">**若要建立屬性提供者**</span><span class="sxs-lookup"><span data-stu-id="50637-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="50637-107">使用 WMI 設計和註冊您的提供者。</span><span class="sxs-lookup"><span data-stu-id="50637-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="50637-108">執行個體提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md)類別，向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="50637-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="50637-109">如需詳細資訊，請參閱 [註冊屬性提供者](registering-a-property-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="50637-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="50637-110">為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="50637-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="50637-111">WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="50637-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="50637-112">這是所有提供者通用的工作。</span><span class="sxs-lookup"><span data-stu-id="50637-112">This is a task common to all providers.</span></span> <span data-ttu-id="50637-113">如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="50637-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="50637-114">強烈建議您使用多執行緒模型「兩者」的屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="50637-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="50637-115">為您的提供者執行 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="50637-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="50637-116">[**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)介面是屬性提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="50637-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="50637-117">這兩種主要方法是 [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) 和 [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty)。</span><span class="sxs-lookup"><span data-stu-id="50637-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="50637-118">如需詳細資訊，請參閱 [執行屬性提供者的主要介面](implementing-the-primary-interface-for-a-property-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="50637-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="50637-119">加入提供者所需的任何其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="50637-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="50637-120">設計您的提供者時，您很可能需要呼叫 WMI 介面。</span><span class="sxs-lookup"><span data-stu-id="50637-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="50637-121">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [維護提供者中的安全性層級](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="50637-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="50637-122">取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="50637-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="50637-123">如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="50637-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="50637-124">以您的新程式碼取代預先存在的提供者。</span><span class="sxs-lookup"><span data-stu-id="50637-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="50637-125">如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="50637-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="50637-126">如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="50637-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



