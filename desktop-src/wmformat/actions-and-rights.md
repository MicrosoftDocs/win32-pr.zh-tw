---
title: 動作和許可權
description: 動作和許可權
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- 數位版權管理 (DRM) ，動作
- DRM (數位版權管理) ，動作
- 數位版權管理 (DRM) ，權利
- DRM (數位版權管理) ，權利
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 授權，DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020916"
---
# <a name="actions-and-rights"></a><span data-ttu-id="bc64f-113">動作和許可權</span><span class="sxs-lookup"><span data-stu-id="bc64f-113">Actions and Rights</span></span>

<span data-ttu-id="bc64f-114">使用 Windows Media DRM 保護檔案時，其使用方式完全受限。</span><span class="sxs-lookup"><span data-stu-id="bc64f-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="bc64f-115">您可以發出授權，讓使用者以特定方式使用內容。</span><span class="sxs-lookup"><span data-stu-id="bc64f-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="bc64f-116">使用者可能使用內容的每種方式都是由動作描述。</span><span class="sxs-lookup"><span data-stu-id="bc64f-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="bc64f-117">例如，在電腦上播放檔案是一個動作。</span><span class="sxs-lookup"><span data-stu-id="bc64f-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="bc64f-118">啟用指定動作的授權稱為授與許可權。</span><span class="sxs-lookup"><span data-stu-id="bc64f-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="bc64f-119">例如，授權可以授與在電腦上播放內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="bc64f-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="bc64f-120">動作和許可權指的是使用內容的相同方式。</span><span class="sxs-lookup"><span data-stu-id="bc64f-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="bc64f-121">不同之處在于動作會參考使用，而許可權則是指許可權。</span><span class="sxs-lookup"><span data-stu-id="bc64f-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="bc64f-122">儘管有此差異，在本檔和描述 Windows Media DRM 的其他檔中，通常會交替使用「動作」和「許可權」等字。</span><span class="sxs-lookup"><span data-stu-id="bc64f-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="bc64f-123">受 Windows Media DRM 許可權規範的動作列在本檔的 [許可權常數](rights-constants.md) 一節中。</span><span class="sxs-lookup"><span data-stu-id="bc64f-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="bc64f-124">Windows Media DRM 用戶端擴充 Api 的某些方法會使用不同的常數來參考基本的 DRM 許可權。</span><span class="sxs-lookup"><span data-stu-id="bc64f-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="bc64f-125">例如， [**IWMDRMLicenseQuery：： QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) 方法會使用一組特定于授權狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="bc64f-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="bc64f-126">雖然這些常數是定義與基本許可權常數不同的字串，但它們會參考授權中的相同許可權。</span><span class="sxs-lookup"><span data-stu-id="bc64f-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc64f-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc64f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc64f-128">**概念**</span><span class="sxs-lookup"><span data-stu-id="bc64f-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




