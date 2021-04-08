---
title: 使用 IWMPCdromRip 介面進行翻錄
description: 使用 IWMPCdromRip 介面進行翻錄
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，IWMPCdromRip 介面
- 將 Cd、IWMPCdromRip 介面翻錄
- IWMPCdromRip 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841908"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="bac2a-113">使用 IWMPCdromRip 介面進行翻錄</span><span class="sxs-lookup"><span data-stu-id="bac2a-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="bac2a-114">本節說明如何使用 [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) 介面，從 CD 翻錄音樂。</span><span class="sxs-lookup"><span data-stu-id="bac2a-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="bac2a-115">使用 **IWMPCdromRip** 介面來將 CD 翻錄，與使用 Windows Media Player 使用者介面來將音樂翻錄的效果相同。</span><span class="sxs-lookup"><span data-stu-id="bac2a-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="bac2a-116">已翻錄的內容會根據使用者的喜好設定自動新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="bac2a-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="bac2a-117">如需 CD 翻錄的詳細資訊，請參閱 Windows Media Player 說明中的「從 Cd 翻錄音樂」。</span><span class="sxs-lookup"><span data-stu-id="bac2a-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="bac2a-118">本節中的程式碼範例會使用 Active Template Library (ATL) 類別，例如 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="bac2a-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="bac2a-119">包含的標頭</span><span class="sxs-lookup"><span data-stu-id="bac2a-119">Included Headers</span></span>

<span data-ttu-id="bac2a-120">若要使用本節中的程式碼，請包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="bac2a-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="bac2a-121">介面指標</span><span class="sxs-lookup"><span data-stu-id="bac2a-121">Interface Pointers</span></span>

<span data-ttu-id="bac2a-122">Windows Media Player 的介面會儲存在下列成員變數中。</span><span class="sxs-lookup"><span data-stu-id="bac2a-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="bac2a-123">下列各節說明如何使用 IWMPCdromRip 介面</span><span class="sxs-lookup"><span data-stu-id="bac2a-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="bac2a-124">擷取轉錄介面</span><span class="sxs-lookup"><span data-stu-id="bac2a-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="bac2a-125">啟動 Rip 進程</span><span class="sxs-lookup"><span data-stu-id="bac2a-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="bac2a-126">正在抓取 Rip 狀態</span><span class="sxs-lookup"><span data-stu-id="bac2a-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="bac2a-127">選取要進行翻錄的專案</span><span class="sxs-lookup"><span data-stu-id="bac2a-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 




