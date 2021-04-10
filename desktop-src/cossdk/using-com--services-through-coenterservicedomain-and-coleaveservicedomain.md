---
description: 透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: 透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111017"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="2cae4-103">透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="2cae4-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="2cae4-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 和 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) 會一起用來圍繞在自己的內容中執行的程式碼區域，而且可以使用 com + 服務，而不需要 com + 元件。</span><span class="sxs-lookup"><span data-stu-id="2cae4-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="2cae4-105">此內容中使用的 COM + 服務是透過傳遞給 **CoEnterServiceDomain** 的 [**CServiceConfig**](cserviceconfig.md)物件來設定。</span><span class="sxs-lookup"><span data-stu-id="2cae4-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="2cae4-106">**CoEnterServiceDomain** 和 **CoLeaveServiceDomain** 所包圍的程式碼，其行為就如同在此內容中建立的物件上呼叫的方法一樣。</span><span class="sxs-lookup"><span data-stu-id="2cae4-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="2cae4-107">腳本應用程式可以使用這組函式來提供 COM + 服務的執行時間支援，而不需要元件。</span><span class="sxs-lookup"><span data-stu-id="2cae4-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="2cae4-108">例如，您可以開發腳本應用程式，以提供允許腳本寫入器在腳本中輸入及保留服務網域的標記。</span><span class="sxs-lookup"><span data-stu-id="2cae4-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="2cae4-109">當腳本引擎處理腳本並遇到標記時，可以使用預先設定的 [**CServiceConfig**](cserviceconfig.md)物件來呼叫 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 、執行必要的程式碼，然後呼叫 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)。</span><span class="sxs-lookup"><span data-stu-id="2cae4-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="2cae4-110">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="2cae4-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="2cae4-111">不適用。</span><span class="sxs-lookup"><span data-stu-id="2cae4-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="2cae4-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2cae4-112">Visual Basic</span></span>

<span data-ttu-id="2cae4-113">不適用。</span><span class="sxs-lookup"><span data-stu-id="2cae4-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="2cae4-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="2cae4-114">C/C++</span></span>

<span data-ttu-id="2cae4-115">下列程式碼片段說明如何在呼叫 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 和 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)之間使用 com + 服務。</span><span class="sxs-lookup"><span data-stu-id="2cae4-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="2cae4-116">為求簡單明瞭，會忽略錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="2cae4-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="2cae4-117">此程式碼片段會使用在 [使用 CServiceConfig 設定 COM + 服務](configuring-com--services-with-cserviceconfig.md)時所建立和設定的 [**CServiceConfig**](cserviceconfig.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2cae4-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a><span data-ttu-id="2cae4-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="2cae4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cae4-119">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="2cae4-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="2cae4-120">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="2cae4-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="2cae4-121">使用 CServiceConfig 設定 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="2cae4-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="2cae4-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="2cae4-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="2cae4-123">透過 CoCreateActivity 使用 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="2cae4-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



