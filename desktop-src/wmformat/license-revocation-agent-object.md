---
title: 授權撤銷代理程式物件
description: 授權撤銷代理程式物件
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media Format SDK、授權撤銷代理程式物件
- Advanced Systems Format (ASF) 、授權撤銷代理程式物件
- ASF (Advanced 系統格式) 、授權撤銷代理程式物件
- 物件、授權撤銷代理程式物件
- 授權撤銷，授權撤銷代理程式物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374390"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="bacae-108">授權撤銷代理程式物件</span><span class="sxs-lookup"><span data-stu-id="bacae-108">License Revocation Agent Object</span></span>

<span data-ttu-id="bacae-109">授權撤銷代理程式物件會管理授權撤銷的用戶端。</span><span class="sxs-lookup"><span data-stu-id="bacae-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="bacae-110">授權撤銷是授權伺服器可以從用戶端電腦上的授權存放區中移除授權的程式。</span><span class="sxs-lookup"><span data-stu-id="bacae-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="bacae-111">此程式牽涉到在用戶端應用程式和授權伺服器之間傳遞數個訊息。</span><span class="sxs-lookup"><span data-stu-id="bacae-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="bacae-112">在此物件上公開的方法會處理並產生這些訊息。</span><span class="sxs-lookup"><span data-stu-id="bacae-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="bacae-113">授權撤銷代理程式物件是由 [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) 函式所建立，該函式會將指標設定為 [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) 介面。</span><span class="sxs-lookup"><span data-stu-id="bacae-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="bacae-114">**IUnknown** 和 **IWMLicenseRevocationAgent** 是此物件唯一支援的介面。</span><span class="sxs-lookup"><span data-stu-id="bacae-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bacae-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="bacae-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bacae-116">**物件**</span><span class="sxs-lookup"><span data-stu-id="bacae-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




