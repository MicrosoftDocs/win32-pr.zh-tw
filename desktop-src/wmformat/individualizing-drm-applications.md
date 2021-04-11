---
title: Individualizing DRM 應用程式
description: Individualizing DRM 應用程式
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media 格式 SDK，individualizing DRM 應用程式
- Windows Media Format SDK，應用程式 individualizing
- Advanced Systems Format (ASF) 、individualizing DRM 應用程式
- ASF (Advanced Systems Format) 、individualizing DRM 應用程式
- Advanced Systems Format (ASF) 、application individualizing
- ASF (Advanced Systems Format) 、application individualizing
- 數位版權管理 (DRM) 、individualizing 應用程式
- DRM (數位版權管理) 、individualizing 應用程式
- 數位版權管理 (DRM) 、應用程式 individualizing
- DRM (數位版權管理) 、應用程式 individualizing
- 應用程式 individualizing
- individualizing DRM 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "103933000"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="ee149-115">Individualizing DRM 應用程式</span><span class="sxs-lookup"><span data-stu-id="ee149-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="ee149-116">為了提高安全性，您可以將應用程式的 DRM 元件 *個人* 化。</span><span class="sxs-lookup"><span data-stu-id="ee149-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="ee149-117">個別的應用程式是已收到升級至其 DRM 元件的應用程式，這些元件會將它與相同應用程式的所有其他複本進行區別。</span><span class="sxs-lookup"><span data-stu-id="ee149-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="ee149-118">內容擁有者可以要求只能在已個人化的應用程式上播放其受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="ee149-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="ee149-119">當應用程式連線到 Microsoft 的「個人化服務」時（接著在使用者的電腦上安裝安全性升級），就會開始進行個人化程式。</span><span class="sxs-lookup"><span data-stu-id="ee149-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="ee149-120">由於「個人」服務會處理來自使用者的資訊，因此您必須在 Microsoft 網站上顯示 Microsoft 隱私權原則或提供該頁面的連結： <https://privacy.microsoft.com/privacystatement> 。</span><span class="sxs-lookup"><span data-stu-id="ee149-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="ee149-121">您可以用不同的方式來完成個人化。</span><span class="sxs-lookup"><span data-stu-id="ee149-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="ee149-122">例如，當使用者播放受保護的檔案時，就可以進行個人化。</span><span class="sxs-lookup"><span data-stu-id="ee149-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="ee149-123">授權要求會傳送至 [*Windows Media 授權服務*](wmformat-glossary.md)，此服務會檢查要求 [*授權*](wmformat-glossary.md)之應用程式的憑證。</span><span class="sxs-lookup"><span data-stu-id="ee149-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="ee149-124">如果應用程式的 DRM 元件尚未進行個人化，Windows Media License Service 會拒絕發出授權，因為這是 Windows Media License Service 的原則，只會將授權發行給個別的玩家。</span><span class="sxs-lookup"><span data-stu-id="ee149-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="ee149-125">然後，應用程式可以通知使用者必須升級應用程式。</span><span class="sxs-lookup"><span data-stu-id="ee149-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="ee149-126">如果使用者同意，則會提供安全性升級，以賦予應用程式的 DRM 元件。</span><span class="sxs-lookup"><span data-stu-id="ee149-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="ee149-127">為了獲得更好的使用者體驗，您可以在安裝期間以安全性升級步驟的形式起始您的個人化程式。然後，使用者在嘗試播放受保護的檔案時，不會中斷以取得安全性升級。</span><span class="sxs-lookup"><span data-stu-id="ee149-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="ee149-128">您也可以將 **安全性升級** 功能表命令或按鈕新增至應用程式，以主動地鼓勵使用。</span><span class="sxs-lookup"><span data-stu-id="ee149-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="ee149-129">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="ee149-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee149-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee149-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee149-131">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="ee149-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="ee149-132">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="ee149-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




