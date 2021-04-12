---
description: 有兩種方式可以實作為類別提供者：將介面實作為推入提供者，或做為提取提供者。
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: 執行類別提供者的主要介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319667"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="85810-103">執行類別提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="85810-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="85810-104">有兩種方式可以實作為類別提供者：將介面實作為推入提供者，或做為提取提供者。</span><span class="sxs-lookup"><span data-stu-id="85810-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="85810-105">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="85810-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="85810-106">執行推播類別提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="85810-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="85810-107">執行提取類別提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="85810-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="85810-108">執行推播類別提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="85810-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="85810-109">雖然所有提供者都是將 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 用於初始化，以及至少一個其他介面作為主要介面，但推送提供者只會執行 **IWbemProviderInit**。</span><span class="sxs-lookup"><span data-stu-id="85810-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="85810-110">確定您的執行會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="85810-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="85810-111">抓取適當的類別資料。</span><span class="sxs-lookup"><span data-stu-id="85810-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="85810-112">將資料放在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="85810-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="85810-113">刪除過時的資料。</span><span class="sxs-lookup"><span data-stu-id="85810-113">Deletes obsolete data.</span></span>

<span data-ttu-id="85810-114">完成初始化程式之後，WMI 會處理屬於推送提供者之類別的所有應用程式要求，而不需要任何進一步的提供者互動。</span><span class="sxs-lookup"><span data-stu-id="85810-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="85810-115">之後，推送提供者會有效地做為 WMI 的用戶端，而不是提供者。</span><span class="sxs-lookup"><span data-stu-id="85810-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="85810-116">如需執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)的詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="85810-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="85810-117">呼叫 WMI 以建立、更新或移除推送提供者中的資料時，請將 *lFlags* 參數設定為在所有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)方法的呼叫中包含 **WBEM \_ 旗標擁有者 \_ \_ 更新** 旗標。</span><span class="sxs-lookup"><span data-stu-id="85810-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="85810-118">執行提取類別提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="85810-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="85810-119">類別提取提供者應該將 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 實作為主要介面。</span><span class="sxs-lookup"><span data-stu-id="85810-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="85810-120">**IWbemServices** 介面支援資料抓取、資料更新、資料移除、列舉和查詢處理。</span><span class="sxs-lookup"><span data-stu-id="85810-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="85810-121">不過，因為 **iwbemservices** 也是由應用程式和提供者用來要求 WMI 服務，所以 **iwbemservices** 包含許多與類別提供者無關的方法。</span><span class="sxs-lookup"><span data-stu-id="85810-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="85810-122">您的執行必須分別透過 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 和 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) 方法支援類別抓取和列舉。</span><span class="sxs-lookup"><span data-stu-id="85810-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="85810-123">下表列出可為類別提供者執行的其他非同步 **IWbemServices** 方法。</span><span class="sxs-lookup"><span data-stu-id="85810-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="85810-124">方法</span><span class="sxs-lookup"><span data-stu-id="85810-124">Method</span></span>                                                     | <span data-ttu-id="85810-125">功能</span><span class="sxs-lookup"><span data-stu-id="85810-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="85810-126">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="85810-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="85810-127">修改</span><span class="sxs-lookup"><span data-stu-id="85810-127">Modification</span></span> |
| [<span data-ttu-id="85810-128">**DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="85810-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="85810-129">刪除</span><span class="sxs-lookup"><span data-stu-id="85810-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="85810-130">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="85810-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="85810-131">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="85810-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="85810-132">您的類別提供者應該提供存根執行，以傳回不支援您的功能集之所有其他 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)方法的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="85810-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="85810-133">具體而言，WMI 不支援類別提供者的查詢處理。</span><span class="sxs-lookup"><span data-stu-id="85810-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="85810-134">因此，類別提供者必須傳回無法執行 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)的 **WBEM \_ E \_ 提供者 \_ \_** 、將其 **QuerySupportLevels** 登錄屬性設為 **Null** 或兩者。</span><span class="sxs-lookup"><span data-stu-id="85810-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="85810-135">類別提供者所執行的介面非常類似于執行個體提供者和方法提供者的介面。</span><span class="sxs-lookup"><span data-stu-id="85810-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="85810-136">事實上，單一提供者可以執行所有方法並正確註冊，以作為三種類型的提供者。</span><span class="sxs-lookup"><span data-stu-id="85810-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



