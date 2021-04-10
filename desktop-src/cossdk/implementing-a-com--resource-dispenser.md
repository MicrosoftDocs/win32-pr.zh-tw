---
description: 執行 COM + 資源配置器
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: 執行 COM + 資源配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111433"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="8eb72-103">執行 COM + 資源配置器</span><span class="sxs-lookup"><span data-stu-id="8eb72-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="8eb72-104">下列步驟概述執行 COM + 資源配置器的一般程式：</span><span class="sxs-lookup"><span data-stu-id="8eb72-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="8eb72-105">決定 **RESTYPID** 格式，以分類資源彼此之間的差異。</span><span class="sxs-lookup"><span data-stu-id="8eb72-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="8eb72-106">分別使用 Mtxdm 和 Mtxdm 標頭檔和程式庫。</span><span class="sxs-lookup"><span data-stu-id="8eb72-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="8eb72-107">建立可執行 [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) 介面的 DLL，以及您想要公開給應用程式的 API。</span><span class="sxs-lookup"><span data-stu-id="8eb72-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="8eb72-108">在啟動 ([*DllMain*](/windows/desktop/Dlls/dllmain) 或第一次呼叫分配 API) ，呼叫 [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) 函數。</span><span class="sxs-lookup"><span data-stu-id="8eb72-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="8eb72-109">這會將指標傳回給分配器管理員的 [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="8eb72-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="8eb72-110">呼叫 [**IDispenserManager：： RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser)，並將指標傳遞至您的 [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)執行。</span><span class="sxs-lookup"><span data-stu-id="8eb72-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="8eb72-111">這會導致分配管理員為您的資源配置器建立 (共用管理員) 的持有者，然後將指標傳回 [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) 介面。</span><span class="sxs-lookup"><span data-stu-id="8eb72-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="8eb72-112">儲存這個指標，讓您可以呼叫 [**IHolder：： AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) 和 [**IHolder：： FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)。</span><span class="sxs-lookup"><span data-stu-id="8eb72-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="8eb72-113">您現在可以 (回應對 API 的呼叫，) 呼叫 [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) 和 [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)。</span><span class="sxs-lookup"><span data-stu-id="8eb72-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="8eb72-114">**AllocResource** 一開始會透過回呼至您的 [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) 方法來回應，但後續的 **AllocResource** 呼叫會從不斷成長的資源集區中提供服務。</span><span class="sxs-lookup"><span data-stu-id="8eb72-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eb72-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8eb72-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb72-116">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="8eb72-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="8eb72-117">COM + 資源配置器介面</span><span class="sxs-lookup"><span data-stu-id="8eb72-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
