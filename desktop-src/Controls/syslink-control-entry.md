---
title: SysLink
description: 本章節包含與 SysLink 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: 13a7b6d0-4bf1-480f-b447-838a550a5866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9bbfaea9b86c2d8dc42c84d050e5bec997ceb18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932054"
---
# <a name="syslink"></a><span data-ttu-id="51112-103">SysLink</span><span class="sxs-lookup"><span data-stu-id="51112-103">SysLink</span></span>

<span data-ttu-id="51112-104">本章節包含與 SysLink 控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="51112-104">This section contains information about the programming elements used with SysLink controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="51112-105">概觀</span><span class="sxs-lookup"><span data-stu-id="51112-105">Overviews</span></span>



| <span data-ttu-id="51112-106">主題</span><span class="sxs-lookup"><span data-stu-id="51112-106">Topic</span></span>                                    | <span data-ttu-id="51112-107">目錄</span><span class="sxs-lookup"><span data-stu-id="51112-107">Contents</span></span>                                                                                       |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51112-108">SysLink 控制項</span><span class="sxs-lookup"><span data-stu-id="51112-108">SysLink Controls</span></span>](syslink-overview.md) | <span data-ttu-id="51112-109">SysLink 控制項提供一個便利的方式，讓您在視窗中內嵌超文字連結。</span><span class="sxs-lookup"><span data-stu-id="51112-109">The SysLink control provides a convenient way to embed hypertext links in a window.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="51112-110">訊息</span><span class="sxs-lookup"><span data-stu-id="51112-110">Messages</span></span>



| <span data-ttu-id="51112-111">主題</span><span class="sxs-lookup"><span data-stu-id="51112-111">Topic</span></span>                                           | <span data-ttu-id="51112-112">目錄</span><span class="sxs-lookup"><span data-stu-id="51112-112">Contents</span></span>                                                                             |
|-------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="51112-113">**LM \_ GETIDEALHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="51112-113">**LM\_GETIDEALHEIGHT**</span></span>](lm-getidealheight.md) | <span data-ttu-id="51112-114">抓取控制項目前寬度之連結的慣用高度。</span><span class="sxs-lookup"><span data-stu-id="51112-114">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="51112-115">**LM \_ GETIDEALSIZE**</span><span class="sxs-lookup"><span data-stu-id="51112-115">**LM\_GETIDEALSIZE**</span></span>](lm-getidealsize.md)     | <span data-ttu-id="51112-116">抓取控制項目前寬度之連結的慣用高度。</span><span class="sxs-lookup"><span data-stu-id="51112-116">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="51112-117">**LM \_ GETITEM**</span><span class="sxs-lookup"><span data-stu-id="51112-117">**LM\_GETITEM**</span></span>](lm-getitem.md)               | <span data-ttu-id="51112-118">抓取專案的狀態和屬性。</span><span class="sxs-lookup"><span data-stu-id="51112-118">Retrieves the states and attributes of an item.</span></span><br/>                           |
| [<span data-ttu-id="51112-119">**LM \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**</span><span class="sxs-lookup"><span data-stu-id="51112-119">**LM\_HITTEST**</span></span>](lm-hittest.md)               | <span data-ttu-id="51112-120">判斷使用者是否按一下指定的連結。</span><span class="sxs-lookup"><span data-stu-id="51112-120">Determines whether the user clicked the specified link.</span></span><br/>                   |
| [<span data-ttu-id="51112-121">**LM \_ SETITEM**</span><span class="sxs-lookup"><span data-stu-id="51112-121">**LM\_SETITEM**</span></span>](lm-setitem.md)               | <span data-ttu-id="51112-122">設定專案的狀態和屬性。</span><span class="sxs-lookup"><span data-stu-id="51112-122">Sets the states and attributes of an item.</span></span><br/>                                |



 

### <a name="structures"></a><span data-ttu-id="51112-123">結構</span><span class="sxs-lookup"><span data-stu-id="51112-123">Structures</span></span>



| <span data-ttu-id="51112-124">主題</span><span class="sxs-lookup"><span data-stu-id="51112-124">Topic</span></span>                                | <span data-ttu-id="51112-125">目錄</span><span class="sxs-lookup"><span data-stu-id="51112-125">Contents</span></span>                                                                                                                                                                           |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51112-126">**LHITTESTINFO**</span><span class="sxs-lookup"><span data-stu-id="51112-126">**LHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lhittestinfo) | <span data-ttu-id="51112-127">用來取得對應至指定位置之連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="51112-127">Used to get information about the link corresponding to a given location.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="51112-128">**LITEM**</span><span class="sxs-lookup"><span data-stu-id="51112-128">**LITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-litem)               | <span data-ttu-id="51112-129">用來設定和取出連結專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="51112-129">Used to set and retrieve information about a link item.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="51112-130">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="51112-130">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)             | <span data-ttu-id="51112-131">[**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink)包含通知資訊。</span><span class="sxs-lookup"><span data-stu-id="51112-131">The [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) Contains notification information.</span></span> <span data-ttu-id="51112-132">以 [nm \_ CLICK](nm-click-syslink.md) 或 [nm \_ RETURN](nm-return.md) 訊息傳送此結構。</span><span class="sxs-lookup"><span data-stu-id="51112-132">Send this structure with the [NM\_CLICK](nm-click-syslink.md) or [NM\_RETURN](nm-return.md) messages.</span></span><br/> |



 

 

 





