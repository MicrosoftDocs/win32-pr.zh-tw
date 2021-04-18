---
title: 執行執行個體提供者主要介面
description: 執行個體提供者會使用 IWbemServices 的非同步方法做為 WMI 的主要介面。
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971502"
---
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="38bab-103">執行執行個體提供者主要介面</span><span class="sxs-lookup"><span data-stu-id="38bab-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="38bab-104">執行個體提供者會使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 的非同步方法做為 WMI 的主要介面。</span><span class="sxs-lookup"><span data-stu-id="38bab-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="38bab-105">藉由只執行滿足您執行個體提供者需求的方法，您可以減少您花費在撰寫程式碼的資源數量。</span><span class="sxs-lookup"><span data-stu-id="38bab-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="38bab-106">不過，藉由針對其他類型的提供者來執行保留的方法，您可以減少您撰寫的提供者數目。</span><span class="sxs-lookup"><span data-stu-id="38bab-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="38bab-107">由於應用程式和提供者也會使用它來要求 WMI 的服務，因此， [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 包含許多與執行個體提供者無關的方法。</span><span class="sxs-lookup"><span data-stu-id="38bab-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="38bab-108">下表列出可為執行個體提供者執行的 **IWbemServices** 方法。</span><span class="sxs-lookup"><span data-stu-id="38bab-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="38bab-109">方法</span><span class="sxs-lookup"><span data-stu-id="38bab-109">Method</span></span>                                                                   | <span data-ttu-id="38bab-110">功能</span><span class="sxs-lookup"><span data-stu-id="38bab-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="38bab-111">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="38bab-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="38bab-112">重建</span><span class="sxs-lookup"><span data-stu-id="38bab-112">Retrieval</span></span>        |
| [<span data-ttu-id="38bab-113">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="38bab-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="38bab-114">修改</span><span class="sxs-lookup"><span data-stu-id="38bab-114">Modification</span></span>     |
| [<span data-ttu-id="38bab-115">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="38bab-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="38bab-116">刪除</span><span class="sxs-lookup"><span data-stu-id="38bab-116">Deletion</span></span>         |
| [<span data-ttu-id="38bab-117">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="38bab-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="38bab-118">列舉型別</span><span class="sxs-lookup"><span data-stu-id="38bab-118">Enumeration</span></span>      |
| [<span data-ttu-id="38bab-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="38bab-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="38bab-120">查詢處理</span><span class="sxs-lookup"><span data-stu-id="38bab-120">Query processing</span></span> |



 

<span data-ttu-id="38bab-121">針對您未使用的方法，您的提供者可以提供可傳回無法使用 **WBEM \_ E \_ 提供 \_ 者 \_** 的存根執行。</span><span class="sxs-lookup"><span data-stu-id="38bab-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="38bab-122">這包括上表未列出的所有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法。</span><span class="sxs-lookup"><span data-stu-id="38bab-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="38bab-123">單一提供者可以透過適當的方式註冊和執行所有相關的方法，以同時作為類別、實例和方法提供者。</span><span class="sxs-lookup"><span data-stu-id="38bab-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="38bab-124">如需詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md) 和 [撰寫方法提供者](writing-a-method-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="38bab-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



