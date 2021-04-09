---
title: DRM 版本
description: DRM 版本
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK，DRM 版本
- 數位版權管理 (DRM) ，版本
- DRM (數位版權管理) ，版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932071"
---
# <a name="drm-versions"></a><span data-ttu-id="1d246-106">DRM 版本</span><span class="sxs-lookup"><span data-stu-id="1d246-106">DRM Versions</span></span>

<span data-ttu-id="1d246-107">有數種版本的 Windows Media 數位版權管理 (DRM) 。</span><span class="sxs-lookup"><span data-stu-id="1d246-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="1d246-108">DRM 第1版通常會與本檔中的其他版本分開設定，因為它是使用與較新版本不同的技術來實行。</span><span class="sxs-lookup"><span data-stu-id="1d246-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="1d246-109">第二次產生的 Windows Media DRM 稱為 DRM 第7版，因為它是 Windows Media Format 7 SDK 的一部分引進的。</span><span class="sxs-lookup"><span data-stu-id="1d246-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="1d246-110">有時也稱為 DRM 第2版。</span><span class="sxs-lookup"><span data-stu-id="1d246-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="1d246-111">較新版本的 Windows Media DRM （DRM 第9版和新的 Windows Media DRM 10）是 DRM 版本7的延伸模組，並使用相同的程式來執行。</span><span class="sxs-lookup"><span data-stu-id="1d246-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="1d246-112">所有版本的 Windows Media DRM 都使用相同的加密常式;版本之間的差異與授權功能有關。</span><span class="sxs-lookup"><span data-stu-id="1d246-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="1d246-113">當您使用 Windows Media Format SDK 的物件建立受保護的檔案時，您應該同時支援第1版與最新版本。</span><span class="sxs-lookup"><span data-stu-id="1d246-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="1d246-114">受 DRM 第1版保護的檔案，與受較新版的檔案（僅限於標頭的內容）所保護的檔案不同。</span><span class="sxs-lookup"><span data-stu-id="1d246-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="1d246-115">包含額外標頭資訊的較新檔案仍可在只轉譯第1版內容的用戶端上使用。</span><span class="sxs-lookup"><span data-stu-id="1d246-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="1d246-116">在較新版本的 DRM 提供較高層級的安全性和其他功能時，仍有許多使用第1版的播放機。</span><span class="sxs-lookup"><span data-stu-id="1d246-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="1d246-117">如需 DRM 版本的詳細資訊，請參閱 Windows Media Rights Manager SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="1d246-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="1d246-118">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="1d246-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1d246-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d246-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d246-120">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="1d246-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1d246-121">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="1d246-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




