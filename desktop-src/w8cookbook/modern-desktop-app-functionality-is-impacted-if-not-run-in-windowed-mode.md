---
title: 如果未在視窗模式中執行，則會影響桌面應用程式功能
description: 在 Windows 10 中，Windows 應用程式預設不再是全螢幕，而是在視窗化和作業（例如最小化、還原、最大化、調整大小 (，以及您一直可以對任何其他傳統 Windows 應用程式) 視窗進行的任何其他作業，現在都可以使用）。
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372472"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="967c5-103">如果未在視窗模式中執行，則會影響桌面應用程式功能</span><span class="sxs-lookup"><span data-stu-id="967c5-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="967c5-104">在 Windows 10 中，Windows 應用程式預設不再是全螢幕，而是在視窗化和作業（例如最小化、還原、最大化、調整大小 (，以及您一直可以對任何其他傳統 Windows 應用程式) 視窗進行的任何其他作業，現在都可以使用）。</span><span class="sxs-lookup"><span data-stu-id="967c5-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="967c5-105">表現</span><span class="sxs-lookup"><span data-stu-id="967c5-105">Manifestations</span></span>

<span data-ttu-id="967c5-106">現在最顯著的變更，就是您可以將大小調整為任意大小，而不只是螢幕的螢幕/高度。</span><span class="sxs-lookup"><span data-stu-id="967c5-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="967c5-107">使用者可以持續將應用程式視窗的大小調整為其喜好 (應用程式的最小視窗大小) 。</span><span class="sxs-lookup"><span data-stu-id="967c5-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="967c5-108">這不同于 Windows 8.0 或 Windows 8.1，調整視窗大小的動作是不連續的動作 (使用者重新調整視窗縮圖的大小，這會導致視窗在使用者認可動作) 之後調整大小。</span><span class="sxs-lookup"><span data-stu-id="967c5-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="967c5-109">現在，當使用者將視窗拖曳 (或其他框線位置時，) 它是連續的調整大小，而應用程式會收到調整資料列大小的訊息，而不是大小變更。</span><span class="sxs-lookup"><span data-stu-id="967c5-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="967c5-110">風險降低</span><span class="sxs-lookup"><span data-stu-id="967c5-110">Mitigations</span></span>

<span data-ttu-id="967c5-111">針對 Windows 8.0 和8.1 應用程式緩解此問題：</span><span class="sxs-lookup"><span data-stu-id="967c5-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="967c5-112">如果應用程式功能中的預期功能已中斷，則使用者的緩和措施是使用標題列右上角的 [移全螢幕] 按鈕 (將應用程式放入全螢幕模式中) 。</span><span class="sxs-lookup"><span data-stu-id="967c5-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="967c5-113">如果應用程式啟動受到影響，但未如預期般開啟，則使用者仍應能切換至 Tablet 模式，以強制應用程式在全螢幕模式下啟動，而不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="967c5-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="967c5-114">處理此情況的最佳方式是變更應用程式，以瞭解它可以調整大小為非監視器大小的位置/高度 (亦即，沒有高度/寬度的硬式編碼資料表，且只預期這些，或預期的硬式編碼比例) 。</span><span class="sxs-lookup"><span data-stu-id="967c5-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="967c5-115">應用程式開發人員應該預期在調整應用程式時，可能會在目前的調整大小訊息出現後立即進行其他調整大小的訊息，因此，如果應用程式在調整大小期間開始動畫，可能會在 (之後，應用程式可能會收到另一個調整大小的訊息，因此請務必確保這種情況不會導致應用程式損毀) </span><span class="sxs-lookup"><span data-stu-id="967c5-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




