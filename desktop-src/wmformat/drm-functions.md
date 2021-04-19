---
title: Microsoft Windows Media DRM 用戶端功能
description: Microsoft Windows Media DRM 用戶端功能
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK，函數
- 數位版權管理 (DRM) ，函數
- DRM (數位版權管理) ，函數
- DRM 用戶端擴充 Api，函數
- 用戶端擴充 Api，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966900"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="234f1-108">Microsoft Windows Media DRM 用戶端功能</span><span class="sxs-lookup"><span data-stu-id="234f1-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="234f1-109">下列函式會實作為 Microsoft Windows Media DRM 用戶端擴充 Api 的一部分。</span><span class="sxs-lookup"><span data-stu-id="234f1-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="234f1-110">函式</span><span class="sxs-lookup"><span data-stu-id="234f1-110">Function</span></span>                                                             | <span data-ttu-id="234f1-111">描述</span><span class="sxs-lookup"><span data-stu-id="234f1-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="234f1-112">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="234f1-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="234f1-113">建立可建立其他 DRM 物件的 class factory。</span><span class="sxs-lookup"><span data-stu-id="234f1-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="234f1-114">此函式不需要來自 Microsoft 的存根程式庫，並會建立不支援受保護 DRM 功能的物件。</span><span class="sxs-lookup"><span data-stu-id="234f1-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="234f1-115">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="234f1-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="234f1-116">建立可建立其他 DRM 物件的 class factory。</span><span class="sxs-lookup"><span data-stu-id="234f1-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="234f1-117">此函式需要來自 Microsoft 的存根程式庫，並建立支援受保護 DRM 功能的物件。</span><span class="sxs-lookup"><span data-stu-id="234f1-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="234f1-118">**WMDRMShutdown**</span><span class="sxs-lookup"><span data-stu-id="234f1-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="234f1-119">釋放 Api 所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="234f1-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="234f1-120">**WMDRMStartup**</span><span class="sxs-lookup"><span data-stu-id="234f1-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="234f1-121">初始化 Api 所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="234f1-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="234f1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="234f1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="234f1-123">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="234f1-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




