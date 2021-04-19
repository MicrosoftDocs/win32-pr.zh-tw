---
description: CoCreateActivity 函式是用來將 batch 工作提交至 COM + 系統。 它允許以腳本為基礎的應用程式支援整個應用程式的 COM + 服務設定。
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: 透過 CoCreateActivity 使用 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970343"
---
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="8c86a-104">透過 CoCreateActivity 使用 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="8c86a-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="8c86a-105">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)函式是用來將 batch 工作提交至 com + 系統。</span><span class="sxs-lookup"><span data-stu-id="8c86a-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="8c86a-106">它允許以腳本為基礎的應用程式支援整個應用程式的 COM + 服務設定。</span><span class="sxs-lookup"><span data-stu-id="8c86a-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="8c86a-107">所需的 COM + 服務是透過傳遞給函式的 [**CServiceConfig**](cserviceconfig.md) 物件來設定。</span><span class="sxs-lookup"><span data-stu-id="8c86a-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="8c86a-108">函數會建立活動物件，並傳回該物件的 [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) 介面。</span><span class="sxs-lookup"><span data-stu-id="8c86a-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="8c86a-109">您可以分別使用 **IServiceActivity** 的 [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall)或 [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall)方法，以同步或非同步方式提交批次工作。</span><span class="sxs-lookup"><span data-stu-id="8c86a-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="8c86a-110">[**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall)介面的指標會傳遞至這些方法的每一個，而批次工作則是由開發人員在 **IServiceCall** 介面的 [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall)方法中執行。</span><span class="sxs-lookup"><span data-stu-id="8c86a-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="8c86a-111">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="8c86a-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="8c86a-112">不適用。</span><span class="sxs-lookup"><span data-stu-id="8c86a-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="8c86a-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8c86a-113">Visual Basic</span></span>

<span data-ttu-id="8c86a-114">不適用。</span><span class="sxs-lookup"><span data-stu-id="8c86a-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="8c86a-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="8c86a-115">C/C++</span></span>

<span data-ttu-id="8c86a-116">下列程式碼片段說明如何透過 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)使用 com + 服務。</span><span class="sxs-lookup"><span data-stu-id="8c86a-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="8c86a-117">為求簡單明瞭，會忽略錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="8c86a-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="8c86a-118">此程式碼片段會使用在 [使用 CServiceConfig 設定 COM + 服務](configuring-com--services-with-cserviceconfig.md)時所建立和設定的 [**CServiceConfig**](cserviceconfig.md)物件。</span><span class="sxs-lookup"><span data-stu-id="8c86a-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="8c86a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c86a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c86a-120">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="8c86a-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="8c86a-121">使用 CServiceConfig 設定 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="8c86a-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="8c86a-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="8c86a-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="8c86a-123">透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="8c86a-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



