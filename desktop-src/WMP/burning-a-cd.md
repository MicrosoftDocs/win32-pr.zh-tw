---
title: 燒錄 CD
description: 燒錄 CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，關於
- 燒錄 Cd，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092548"
---
# <a name="burning-a-cd"></a><span data-ttu-id="e1d87-112">燒錄 CD</span><span class="sxs-lookup"><span data-stu-id="e1d87-112">Burning a CD</span></span>

<span data-ttu-id="e1d87-113">本節說明如何使用 [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) 介面將音樂燒錄至 CD。</span><span class="sxs-lookup"><span data-stu-id="e1d87-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="e1d87-114">**IWMPCdromBurn** 介面提供將播放清單燒錄至 cd 的功能，以作為資料或音訊播放軌，以及清除 cd RWs。</span><span class="sxs-lookup"><span data-stu-id="e1d87-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="e1d87-115">程式碼使用方式</span><span class="sxs-lookup"><span data-stu-id="e1d87-115">Code Usage</span></span>

<span data-ttu-id="e1d87-116">本節中的程式碼範例會使用 Active Template Library (ATL) 類別，例如 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="e1d87-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="e1d87-117">包含的標頭</span><span class="sxs-lookup"><span data-stu-id="e1d87-117">Included Headers</span></span>

<span data-ttu-id="e1d87-118">若要使用本節中的程式碼，請包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="e1d87-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="e1d87-119">介面指標</span><span class="sxs-lookup"><span data-stu-id="e1d87-119">Interface Pointers</span></span>

<span data-ttu-id="e1d87-120">Windows Media Player 的介面會儲存在下列成員變數中：</span><span class="sxs-lookup"><span data-stu-id="e1d87-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="e1d87-121">下列主題描述如何使用 CD 燒錄 API。</span><span class="sxs-lookup"><span data-stu-id="e1d87-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="e1d87-122">擷取 CD 燒錄介面</span><span class="sxs-lookup"><span data-stu-id="e1d87-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="e1d87-123">啟動燒錄流程</span><span class="sxs-lookup"><span data-stu-id="e1d87-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="e1d87-124">清除可讀寫 CD</span><span class="sxs-lookup"><span data-stu-id="e1d87-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="e1d87-125">正在抓取磁片磁碟機和光碟狀態</span><span class="sxs-lookup"><span data-stu-id="e1d87-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="e1d87-126">正在取出燒錄狀態</span><span class="sxs-lookup"><span data-stu-id="e1d87-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="e1d87-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1d87-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1d87-128">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="e1d87-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




