---
description: 在繪製之前，系統必須為繪圖作業準備顯示裝置。
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: 顯示裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972701"
---
# <a name="display-devices"></a><span data-ttu-id="4348e-103">顯示裝置</span><span class="sxs-lookup"><span data-stu-id="4348e-103">Display Devices</span></span>

<span data-ttu-id="4348e-104">在繪製之前，系統必須為繪圖作業準備顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="4348e-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="4348e-105">顯示裝置內容會定義一組繪圖物件和其相關聯的屬性，以及影響輸出的圖形模式。</span><span class="sxs-lookup"><span data-stu-id="4348e-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="4348e-106">系統會準備每個顯示裝置內容，以便輸出至視窗、設定視窗的繪圖物件、色彩和模式，而不是顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="4348e-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="4348e-107">當應用程式透過呼叫 GDI 函式提供顯示裝置內容時，GDI 會使用內容中的資訊在指定的視窗中產生輸出，而不侵其他視窗或螢幕的其他部分。</span><span class="sxs-lookup"><span data-stu-id="4348e-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="4348e-108">系統提供五種類型的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="4348e-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="4348e-109">類型</span><span class="sxs-lookup"><span data-stu-id="4348e-109">Type</span></span>                                           | <span data-ttu-id="4348e-110">意義</span><span class="sxs-lookup"><span data-stu-id="4348e-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4348e-111">常見</span><span class="sxs-lookup"><span data-stu-id="4348e-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="4348e-112">允許在指定視窗的工作區中繪製。</span><span class="sxs-lookup"><span data-stu-id="4348e-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="4348e-113">class</span><span class="sxs-lookup"><span data-stu-id="4348e-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="4348e-114">允許在指定視窗的工作區中繪製。</span><span class="sxs-lookup"><span data-stu-id="4348e-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="4348e-115">parent</span><span class="sxs-lookup"><span data-stu-id="4348e-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="4348e-116">允許在視窗中的任何位置繪製。</span><span class="sxs-lookup"><span data-stu-id="4348e-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="4348e-117">雖然父裝置內容也允許在父視窗中繪製，但無法以這種方式使用。</span><span class="sxs-lookup"><span data-stu-id="4348e-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="4348e-118">私人</span><span class="sxs-lookup"><span data-stu-id="4348e-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="4348e-119">允許在指定視窗的工作區中繪製。</span><span class="sxs-lookup"><span data-stu-id="4348e-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="4348e-120">視窗</span><span class="sxs-lookup"><span data-stu-id="4348e-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="4348e-121">允許在視窗中的任何位置繪製。</span><span class="sxs-lookup"><span data-stu-id="4348e-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="4348e-122">系統會根據該視窗類別樣式中所指定的顯示裝置內容類型，提供通用、類別、父系或私用裝置內容至視窗。</span><span class="sxs-lookup"><span data-stu-id="4348e-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="4348e-123">系統只會在應用程式明確要求時（例如，藉由呼叫 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式），提供視窗裝置內容。</span><span class="sxs-lookup"><span data-stu-id="4348e-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="4348e-124">在所有情況下，應用程式都可以使用 [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) 函式來判斷顯示 DC 目前表示的視窗。</span><span class="sxs-lookup"><span data-stu-id="4348e-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="4348e-125">本節提供下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4348e-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="4348e-126">顯示裝置內容快取</span><span class="sxs-lookup"><span data-stu-id="4348e-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="4348e-127">顯示裝置內容預設值</span><span class="sxs-lookup"><span data-stu-id="4348e-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="4348e-128">一般顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="4348e-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="4348e-129">私用顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="4348e-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="4348e-130">父代顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="4348e-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="4348e-131">類別顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="4348e-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="4348e-132">視窗顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="4348e-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="4348e-133">父代顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="4348e-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



