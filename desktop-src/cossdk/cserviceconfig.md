---
description: 指定和設定在呼叫 CoCreateActivity 或 CoEnterServiceDomain 時所輸入的服務網域中要使用的服務。
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: 'CServiceConfig 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991798"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="ba709-103">CServiceConfig 類別</span><span class="sxs-lookup"><span data-stu-id="ba709-103">CServiceConfig class</span></span>

<span data-ttu-id="ba709-104">指定和設定在呼叫 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 或 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)時所輸入的服務網域中要使用的服務。</span><span class="sxs-lookup"><span data-stu-id="ba709-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ba709-105">執行時機</span><span class="sxs-lookup"><span data-stu-id="ba709-105">When to implement</span></span>

<span data-ttu-id="ba709-106">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="ba709-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="ba709-107">需求</span><span class="sxs-lookup"><span data-stu-id="ba709-107">Requirement</span></span> | <span data-ttu-id="ba709-108">值</span><span class="sxs-lookup"><span data-stu-id="ba709-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba709-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="ba709-109">CLSID</span></span>      | <span data-ttu-id="ba709-110">CLSID \_ CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="ba709-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ba709-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="ba709-111">ProgID</span></span>     | <span data-ttu-id="ba709-112">L "COMSVCS。CServiceConfig"</span><span class="sxs-lookup"><span data-stu-id="ba709-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ba709-113">介面</span><span class="sxs-lookup"><span data-stu-id="ba709-113">Interfaces</span></span> | [<span data-ttu-id="ba709-114">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="ba709-115">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="ba709-116">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="ba709-117">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="ba709-118">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="ba709-119">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="ba709-120">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="ba709-121">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="ba709-122">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="ba709-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="ba709-123">使用時機</span><span class="sxs-lookup"><span data-stu-id="ba709-123">When to use</span></span>

<span data-ttu-id="ba709-124">使用這個類別來設定您想要使用的服務。</span><span class="sxs-lookup"><span data-stu-id="ba709-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="ba709-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 和 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 可讓您使用此類別所設定的服務，而不需要先將這些服務系結至元件，再加以使用。</span><span class="sxs-lookup"><span data-stu-id="ba709-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="ba709-126">此類別不是設計用來 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="ba709-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba709-127">備註</span><span class="sxs-lookup"><span data-stu-id="ba709-127">Remarks</span></span>

<span data-ttu-id="ba709-128">若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="ba709-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="ba709-129">從 **CServiceConfig** 類別具現化的物件會匯總無限制執行緒封送處理器，使其可由系統執行時間儲存並重複使用於不同的單元中。</span><span class="sxs-lookup"><span data-stu-id="ba709-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="ba709-130">若要設定個別服務，請呼叫與服務相關聯之介面的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後呼叫該介面上的方法來建立適當的設定。</span><span class="sxs-lookup"><span data-stu-id="ba709-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba709-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba709-131">Requirements</span></span>



| <span data-ttu-id="ba709-132">需求</span><span class="sxs-lookup"><span data-stu-id="ba709-132">Requirement</span></span> | <span data-ttu-id="ba709-133">值</span><span class="sxs-lookup"><span data-stu-id="ba709-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ba709-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba709-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ba709-135">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba709-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ba709-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba709-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ba709-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba709-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ba709-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ba709-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba709-139"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba709-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba709-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba709-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba709-141">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="ba709-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="ba709-142">**CoCreateFreeThreadedMarshaler**</span><span class="sxs-lookup"><span data-stu-id="ba709-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="ba709-143">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="ba709-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="ba709-144">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="ba709-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="ba709-145">沒有元件的 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="ba709-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

