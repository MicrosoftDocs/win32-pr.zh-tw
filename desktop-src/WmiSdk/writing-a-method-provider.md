---
description: 方法提供者允許 WMI 存取類別的方法。 例如，代表應用程式的類別可能會有一個終止應用程式的方法。
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: 撰寫方法提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975029"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="38c31-104">撰寫方法提供者</span><span class="sxs-lookup"><span data-stu-id="38c31-104">Writing a Method Provider</span></span>

<span data-ttu-id="38c31-105">方法提供者允許 WMI 存取類別的方法。</span><span class="sxs-lookup"><span data-stu-id="38c31-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="38c31-106">例如，代表應用程式的類別可能會有一個終止應用程式的方法。</span><span class="sxs-lookup"><span data-stu-id="38c31-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="38c31-107">在更新現有的方法提供者時，變更方法輸入和輸出參數的順序，可能會導致呼叫方法的應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="38c31-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="38c31-108">輸入或輸出參數的順序，是由每個參數上的 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號值所建立。</span><span class="sxs-lookup"><span data-stu-id="38c31-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="38c31-109">第一個參數的 **識別碼** 值為零。</span><span class="sxs-lookup"><span data-stu-id="38c31-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="38c31-110">在現有參數的結尾加入新的輸入參數，而不是將它們插入已建立的序列中。</span><span class="sxs-lookup"><span data-stu-id="38c31-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="38c31-111">下列程式描述如何執行方法提供者。</span><span class="sxs-lookup"><span data-stu-id="38c31-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="38c31-112">**若要執行方法提供者**</span><span class="sxs-lookup"><span data-stu-id="38c31-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="38c31-113">使用 WMI 設計和註冊您的類別提供者。</span><span class="sxs-lookup"><span data-stu-id="38c31-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="38c31-114">類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)類別，向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="38c31-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="38c31-115">如需詳細資訊，請參閱 [註冊方法提供者](registering-a-method-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="38c31-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="38c31-116">為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="38c31-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="38c31-117">強烈建議您使用方法提供者來使用多執行緒模型「兩者」。</span><span class="sxs-lookup"><span data-stu-id="38c31-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="38c31-118">為您的提供者執行 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="38c31-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="38c31-119">[**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面是方法提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="38c31-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="38c31-120">如需詳細資訊，請參閱 [執行方法提供者的主要介面](implementing-the-primary-interface-for-a-method-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="38c31-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="38c31-121">加入提供者所需的任何其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="38c31-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="38c31-122">設計您的提供者時，您很可能需要呼叫 WMI 介面。</span><span class="sxs-lookup"><span data-stu-id="38c31-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="38c31-123">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [維護提供者中的安全性層級](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="38c31-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="38c31-124">取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="38c31-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="38c31-125">如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="38c31-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="38c31-126">以您的新程式碼取代預先存在的提供者。</span><span class="sxs-lookup"><span data-stu-id="38c31-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="38c31-127">如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="38c31-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="38c31-128">如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="38c31-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



