---
description: 下列函式提供多個監視器的支援。
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: 多重顯示器監視函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972640"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="a1719-103">多重顯示器監視函式</span><span class="sxs-lookup"><span data-stu-id="a1719-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="a1719-104">下列函式提供多個監視器的支援。</span><span class="sxs-lookup"><span data-stu-id="a1719-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="a1719-105">函式</span><span class="sxs-lookup"><span data-stu-id="a1719-105">Function</span></span>                                           | <span data-ttu-id="a1719-106">描述</span><span class="sxs-lookup"><span data-stu-id="a1719-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1719-107">**EnumDisplayMonitors**</span><span class="sxs-lookup"><span data-stu-id="a1719-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="a1719-108">列舉與指定裁剪矩形交集以及裝置內容可見區域交集形成之區域的顯示監視器。</span><span class="sxs-lookup"><span data-stu-id="a1719-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="a1719-109">**GetMonitorInfo**</span><span class="sxs-lookup"><span data-stu-id="a1719-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="a1719-110">抓取顯示監視器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1719-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="a1719-111">**MonitorEnumProc**</span><span class="sxs-lookup"><span data-stu-id="a1719-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="a1719-112">[**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)函式所呼叫的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a1719-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="a1719-113">**MonitorFromPoint**</span><span class="sxs-lookup"><span data-stu-id="a1719-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="a1719-114">抓取顯示監視器的控制碼，其中包含指定的點。</span><span class="sxs-lookup"><span data-stu-id="a1719-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="a1719-115">**MonitorFromRect**</span><span class="sxs-lookup"><span data-stu-id="a1719-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="a1719-116">使用指定的矩形，抓取具有最大區域交集的顯示監視器控制碼。</span><span class="sxs-lookup"><span data-stu-id="a1719-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="a1719-117">**MonitorFromWindow**</span><span class="sxs-lookup"><span data-stu-id="a1719-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="a1719-118">抓取顯示監視器的控制碼，該控點與指定視窗的周框有最大的交集區域。</span><span class="sxs-lookup"><span data-stu-id="a1719-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



