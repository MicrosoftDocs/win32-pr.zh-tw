---
description: 更新區域會識別已過期或無效且需要重繪的視窗部分。
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: 更新區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991770"
---
# <a name="the-update-region"></a><span data-ttu-id="ebd02-103">更新區域</span><span class="sxs-lookup"><span data-stu-id="ebd02-103">The Update Region</span></span>

<span data-ttu-id="ebd02-104">*更新區域* 會識別已過期或無效且需要重繪的視窗部分。</span><span class="sxs-lookup"><span data-stu-id="ebd02-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="ebd02-105">系統會使用更新區域來產生適用于應用程式的 [**WM \_ 油漆**](wm-paint.md) 訊息，並將應用程式的最新內容帶入最新的時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="ebd02-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="ebd02-106">系統只會將不正確視窗部分新增至更新區域，因此只需要繪製該部分。</span><span class="sxs-lookup"><span data-stu-id="ebd02-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="ebd02-107">當系統判斷某個視窗需要更新時，會將更新區域的維度設定為視窗的無效部分。</span><span class="sxs-lookup"><span data-stu-id="ebd02-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="ebd02-108">設定更新區域不會立即讓應用程式進行繪製。</span><span class="sxs-lookup"><span data-stu-id="ebd02-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="ebd02-109">相反地，應用程式會繼續從應用程式訊息佇列中取出訊息，直到沒有訊息保留為止。</span><span class="sxs-lookup"><span data-stu-id="ebd02-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="ebd02-110">系統接著會檢查更新區域，如果區域不是空的 (非 Null) ，它就會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="ebd02-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="ebd02-111">應用程式可以使用更新區域來產生其 [**WM \_ 繪製**](wm-paint.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="ebd02-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="ebd02-112">例如，從開啟的檔案載入資料的應用程式通常會在載入時設定更新區域，以便在處理下一個 **WM \_ 油漆** 訊息時繪製新的資料。</span><span class="sxs-lookup"><span data-stu-id="ebd02-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="ebd02-113">一般來說，應用程式不應該在其資料變更時繪製，而是透過 **WM \_ 油漆** 訊息來路由所有繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="ebd02-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



