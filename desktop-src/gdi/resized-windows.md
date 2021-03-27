---
description: 當使用者選擇視窗功能表命令時（例如大小和最大化），或應用程式呼叫函式（例如 SetWindowPos 函式）時，系統會變更視窗的大小。
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: 調整視窗大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848545"
---
# <a name="resized-windows"></a><span data-ttu-id="833b3-103">調整視窗大小</span><span class="sxs-lookup"><span data-stu-id="833b3-103">Resized Windows</span></span>

<span data-ttu-id="833b3-104">當使用者選擇視窗功能表命令時（例如大小和最大化），或應用程式呼叫函式（例如 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 函式）時，系統會變更視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="833b3-104">The system changes the size of a window when the user chooses window menu commands, such as Size and Maximize, or when the application calls functions, such as the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function.</span></span> <span data-ttu-id="833b3-105">當視窗變更大小時，系統會假設先前公開的視窗部分內容不受影響，且不需要重新繪製。</span><span class="sxs-lookup"><span data-stu-id="833b3-105">When a window changes size, the system assumes that the contents of the previously exposed portion of the window are not affected and need not be redrawn.</span></span> <span data-ttu-id="833b3-106">系統只會使視窗中新公開的部分失效，這可節省應用程式處理最終 [**WM \_ 油漆**](wm-paint.md) 訊息的時間。</span><span class="sxs-lookup"><span data-stu-id="833b3-106">The system invalidates only the newly exposed portion of the window, which saves time when the eventual [**WM\_PAINT**](wm-paint.md) message is processed by the application.</span></span> <span data-ttu-id="833b3-107">在此情況下，當視窗的大小減少時，不會產生 **WM \_ 油漆** 。</span><span class="sxs-lookup"><span data-stu-id="833b3-107">In this case, **WM\_PAINT** is not generated when the size of the window is reduced.</span></span>

<span data-ttu-id="833b3-108">針對某些視窗，對視窗大小所做的任何變更都會使內容失效。</span><span class="sxs-lookup"><span data-stu-id="833b3-108">For some windows, any change to the size of the window invalidates the contents.</span></span> <span data-ttu-id="833b3-109">例如，將時鐘臉部調整成整齊顯示在其視窗內的時鐘應用程式，必須在視窗變更大小時重繪時鐘。</span><span class="sxs-lookup"><span data-stu-id="833b3-109">For example, a clock application that adapts the face of the clock to fit neatly within its window must redraw the clock whenever the window changes size.</span></span> <span data-ttu-id="833b3-110">當您在進行垂直、水準或垂直和水準變更時，若要強制系統使視窗的整個工作區失效，應用程式必須在 \_ 註冊視窗類別時指定 cs VREDRAW 或 cs \_ HREDRAW 樣式。</span><span class="sxs-lookup"><span data-stu-id="833b3-110">To force the system to invalidate the entire client area of the window when a vertical, horizontal, or both vertical and horizontal change is made, an application must specify the CS\_VREDRAW or CS\_HREDRAW style, or both, when registering the window class.</span></span> <span data-ttu-id="833b3-111">每次使用者或應用程式變更視窗的大小時，任何屬於具有這些樣式之視窗類別的視窗都會失效。</span><span class="sxs-lookup"><span data-stu-id="833b3-111">Any window belonging to a window class having these styles is invalidated each time the user or the application changes the size of the window.</span></span>

 

 
