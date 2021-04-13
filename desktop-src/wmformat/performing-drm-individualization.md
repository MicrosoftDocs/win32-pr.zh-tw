---
title: 執行 DRM 的個人化
description: 執行 DRM 的個人化
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 的個人化
- Windows Media Format SDK，個人化
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) 、個人化
- DRM (數位版權管理) 、個人化
- 數位版權管理 (DRM) ，DRM 的個人化
- DRM (數位版權管理) ，DRM 的個人化
- DRM 用戶端擴充 Api，個人化
- 用戶端擴充 Api，個人化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301735"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="92272-122">執行 DRM 的個人化</span><span class="sxs-lookup"><span data-stu-id="92272-122">Performing DRM Individualization</span></span>

<span data-ttu-id="92272-123">「個人化」是在用戶端電腦上更新 DRM 元件、將其加密以及使其成為唯一的程式。</span><span class="sxs-lookup"><span data-stu-id="92272-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="92272-124">當電腦是個人化的時，DRM 元件會系結至電腦，而且無法在任何其他電腦上將內容解碼。</span><span class="sxs-lookup"><span data-stu-id="92272-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="92272-125">Windows Media DRM 用戶端擴充 Api 提供在用戶端電腦上 individualizing DRM 元件的支援。</span><span class="sxs-lookup"><span data-stu-id="92272-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="92272-126">藉由呼叫 [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 方法來執行個人化。</span><span class="sxs-lookup"><span data-stu-id="92272-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="92272-127">您可以呼叫 **PerformSecurityUpdate** ，只有當伺服器上的版本比用戶端電腦上安裝的版本還要新時，才會賦予，或者，您可以在不考慮相對安全性版本的情況下強制執行個人化。</span><span class="sxs-lookup"><span data-stu-id="92272-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="92272-128">視需要的個人化旗標是 WMDRM \_ 安全性 \_ 執行 \_ INDIV。</span><span class="sxs-lookup"><span data-stu-id="92272-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="92272-129">強制執行的個人化旗標為 WMDRM \_ 安全性 \_ 執行 \_ 強制 \_ INDIV。</span><span class="sxs-lookup"><span data-stu-id="92272-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="92272-130">**PerformSecurityUpdate** 是非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="92272-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="92272-131">它會快速傳回，然後產生事件，以提供有關「個人化」程式的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="92272-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="92272-132">大部分產生的事件將會是 **MEWMDRMIndividualizationProgress** 事件，每個事件都有相關聯的 [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="92272-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="92272-133">若要取得狀態介面，您必須呼叫 **IMFMediaEvent：： GetValue** 來取出位於相同物件上的 **IUnknown** 指標，然後查詢它以進行 **IWMDRMIndividualizationStatus**。</span><span class="sxs-lookup"><span data-stu-id="92272-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="92272-134">您可以藉由呼叫 [**IWMDRMIndividualizeStatus：： GetStatus**](iwmdrmindividualizationstatus-getstatus.md)，取得 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md)結構的資料。</span><span class="sxs-lookup"><span data-stu-id="92272-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="92272-135">每個產生的事件都有自己的物件，其狀態為，因此您必須逐一查看取得事件值，並每次查詢狀態介面的流程。</span><span class="sxs-lookup"><span data-stu-id="92272-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="92272-136">視下載的大小而定，可能會有數十個或數百個 **MEWMDRMIndividualizationProgress** 事件。</span><span class="sxs-lookup"><span data-stu-id="92272-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="92272-137">當「個人化」程式完成時，就會產生 **MEWMDRMIndividualizationCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="92272-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="92272-138">當個人化完成時，唯一會反映新的個人化狀態的現有物件就是繼承自 [**IWMDRMSecurity**](iwmdrmsecurity.md)的物件。</span><span class="sxs-lookup"><span data-stu-id="92272-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="92272-139">所有其他現有的物件將不會更新。</span><span class="sxs-lookup"><span data-stu-id="92272-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="92272-140">您必須釋放並重新建立任何其他物件，使其反映新的個別狀態。</span><span class="sxs-lookup"><span data-stu-id="92272-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92272-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="92272-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92272-142">**DRM 的個人化範例**</span><span class="sxs-lookup"><span data-stu-id="92272-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="92272-143">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="92272-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="92272-144">**使用媒體基礎事件模型**</span><span class="sxs-lookup"><span data-stu-id="92272-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="92272-145">[Windows Media DRM 的個人化最佳作法](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="92272-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 




