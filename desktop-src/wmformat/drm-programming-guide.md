---
title: Microsoft Windows Media DRM 用戶端程式設計指南
description: Microsoft Windows Media DRM 用戶端程式設計指南
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，程式設計手冊
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) ，程式設計指南
- DRM (數位版權管理) ，程式設計手冊
- DRM 用戶端擴充 Api，關於
- 用戶端擴充 Api，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464088"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="b52d2-119">Microsoft Windows Media DRM 用戶端程式設計指南</span><span class="sxs-lookup"><span data-stu-id="b52d2-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="b52d2-120">本指南提供在您的應用程式中使用 Windows Media DRM 用戶端擴充 Api 功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b52d2-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="b52d2-121">下列各節詳細說明執行 DRM 功能時所牽涉到的步驟。</span><span class="sxs-lookup"><span data-stu-id="b52d2-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="b52d2-122">區段</span><span class="sxs-lookup"><span data-stu-id="b52d2-122">Section</span></span>                                                                                                                          | <span data-ttu-id="b52d2-123">描述</span><span class="sxs-lookup"><span data-stu-id="b52d2-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b52d2-124">快速入門</span><span class="sxs-lookup"><span data-stu-id="b52d2-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="b52d2-125">提供設定 c + + 專案的相關資訊，這些專案使用 Windows Media DRM 用戶端擴充 Api。</span><span class="sxs-lookup"><span data-stu-id="b52d2-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="b52d2-126">取得授權</span><span class="sxs-lookup"><span data-stu-id="b52d2-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="b52d2-127">描述如何在用戶端電腦上取得授權。</span><span class="sxs-lookup"><span data-stu-id="b52d2-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="b52d2-128">從本機授權存放中的授權取得資訊</span><span class="sxs-lookup"><span data-stu-id="b52d2-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="b52d2-129">說明如何取得受保護內容之許可權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b52d2-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="b52d2-130">執行 DRM 的個人化</span><span class="sxs-lookup"><span data-stu-id="b52d2-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="b52d2-131">說明如何更新和賦予用戶端電腦上的 DRM 元件，讓它更安全。</span><span class="sxs-lookup"><span data-stu-id="b52d2-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="b52d2-132">DRM 匯出</span><span class="sxs-lookup"><span data-stu-id="b52d2-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="b52d2-133">說明如何匯出 Windows Media DRM 所保護的內容。</span><span class="sxs-lookup"><span data-stu-id="b52d2-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="b52d2-134">DRM 匯入</span><span class="sxs-lookup"><span data-stu-id="b52d2-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="b52d2-135">說明如何匯入受 Windows Media DRM 保護的內容。</span><span class="sxs-lookup"><span data-stu-id="b52d2-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="b52d2-136">授權撤銷</span><span class="sxs-lookup"><span data-stu-id="b52d2-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="b52d2-137">說明如何從本機授權存放區移除授權。</span><span class="sxs-lookup"><span data-stu-id="b52d2-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="b52d2-138">自動化元件撤銷和更新</span><span class="sxs-lookup"><span data-stu-id="b52d2-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="b52d2-139">描述使用內容啟用的 Windows Media DRM 自動撤銷和更新系統。</span><span class="sxs-lookup"><span data-stu-id="b52d2-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="b52d2-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="b52d2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b52d2-141">**Windows Media DRM 用戶端擴充 Api**</span><span class="sxs-lookup"><span data-stu-id="b52d2-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="b52d2-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b52d2-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
