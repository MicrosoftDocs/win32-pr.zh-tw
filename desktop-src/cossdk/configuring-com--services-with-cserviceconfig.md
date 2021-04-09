---
description: 使用 CServiceConfig 設定 COM + 服務
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: 使用 CServiceConfig 設定 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688703"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="96035-103">使用 CServiceConfig 設定 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="96035-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="96035-104">[**CServiceConfig**](cserviceconfig.md)類別是用來設定可在沒有元件的情況下使用的 com + 服務。</span><span class="sxs-lookup"><span data-stu-id="96035-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="96035-105">它會匯總無限制執行緒封送處理器，讓它可以在不同的單元中使用。</span><span class="sxs-lookup"><span data-stu-id="96035-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="96035-106">若要設定個別的服務，您必須針對與服務相關聯的介面呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後呼叫該介面上的方法來建立適當的設定。</span><span class="sxs-lookup"><span data-stu-id="96035-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="96035-107">下表說明透過 **CServiceConfig** 類別所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="96035-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="96035-108">介面</span><span class="sxs-lookup"><span data-stu-id="96035-108">Interface</span></span>                                                                         | <span data-ttu-id="96035-109">描述</span><span class="sxs-lookup"><span data-stu-id="96035-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96035-110">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="96035-111">類別的預設介面。</span><span class="sxs-lookup"><span data-stu-id="96035-111">The default interface for the class.</span></span> <span data-ttu-id="96035-112">它可用來快速初始化許多 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="96035-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="96035-113">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="96035-114">用來設定 COM 交易整合器 (COMTI) 內建函式資訊。</span><span class="sxs-lookup"><span data-stu-id="96035-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="96035-115">COMTI 可讓開發人員將大型主機交易程式與以元件為基礎的應用程式整合。</span><span class="sxs-lookup"><span data-stu-id="96035-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="96035-116">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="96035-117">用來設定 Internet Information Services (IIS) 內建函式的資訊。</span><span class="sxs-lookup"><span data-stu-id="96035-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="96035-118">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="96035-119">用來設定如何搭配服務使用 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="96035-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="96035-120">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="96035-121">用來設定並存元件。</span><span class="sxs-lookup"><span data-stu-id="96035-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="96035-122">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="96035-123">用來設定 COM + 同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="96035-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="96035-124">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="96035-125">用來設定 COM + 服務的執行緒集區。</span><span class="sxs-lookup"><span data-stu-id="96035-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="96035-126">只有在使用 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 函數時，才能設定執行緒集區。</span><span class="sxs-lookup"><span data-stu-id="96035-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="96035-127">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="96035-128">用來設定追蹤器屬性。</span><span class="sxs-lookup"><span data-stu-id="96035-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="96035-129">追蹤器是一種報告機制，可讓監視程式碼監看正在執行的程式碼。</span><span class="sxs-lookup"><span data-stu-id="96035-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="96035-130">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="96035-131">用來設定 COM + 交易服務。</span><span class="sxs-lookup"><span data-stu-id="96035-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="96035-132">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="96035-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="96035-133">不適用。</span><span class="sxs-lookup"><span data-stu-id="96035-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="96035-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="96035-134">Visual Basic</span></span>

<span data-ttu-id="96035-135">不適用。</span><span class="sxs-lookup"><span data-stu-id="96035-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="96035-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="96035-136">C/C++</span></span>

<span data-ttu-id="96035-137">下列程式碼片段說明如何建立和設定 [**CServiceConfig**](cserviceconfig.md) 物件，以使用 com + 交易。</span><span class="sxs-lookup"><span data-stu-id="96035-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="96035-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="96035-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96035-139">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="96035-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="96035-140">透過 CoCreateActivity 使用 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="96035-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="96035-141">透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="96035-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

