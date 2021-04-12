---
description: 您可以使用 WM \_ 油漆訊息來執行顯示資訊所需的繪圖。
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: 使用 WM_PAINT 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192390"
---
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="be1eb-103">使用 WM \_ 油漆訊息</span><span class="sxs-lookup"><span data-stu-id="be1eb-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="be1eb-104">您可以使用 [**WM \_ 油漆**](wm-paint.md) 訊息來執行顯示資訊所需的繪圖。</span><span class="sxs-lookup"><span data-stu-id="be1eb-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="be1eb-105">因為 \_ 當您的視窗必須更新或您明確要求更新時，系統會將 WM 繪製訊息傳送至您的應用程式，因此您可以合併程式碼，以在應用程式的視窗程式中進行繪製。</span><span class="sxs-lookup"><span data-stu-id="be1eb-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="be1eb-106">只要您的應用程式必須繪製新的或現有的資訊，您就可以使用此程式碼。</span><span class="sxs-lookup"><span data-stu-id="be1eb-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="be1eb-107">下列各節顯示使用 WM \_ 油漆訊息在視窗中繪製的各種方式：</span><span class="sxs-lookup"><span data-stu-id="be1eb-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="be1eb-108">在工作區中繪圖</span><span class="sxs-lookup"><span data-stu-id="be1eb-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="be1eb-109">重繪整個工作區</span><span class="sxs-lookup"><span data-stu-id="be1eb-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="be1eb-110">更新區域中的重繪</span><span class="sxs-lookup"><span data-stu-id="be1eb-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="be1eb-111">使工作區失效</span><span class="sxs-lookup"><span data-stu-id="be1eb-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="be1eb-112">繪製最小化視窗</span><span class="sxs-lookup"><span data-stu-id="be1eb-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="be1eb-113">繪製自訂視窗背景</span><span class="sxs-lookup"><span data-stu-id="be1eb-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 



