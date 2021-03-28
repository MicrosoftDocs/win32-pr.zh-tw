---
description: 有兩種類型的筆刷：邏輯和實體。
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: 關於筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114249"
---
# <a name="about-brushes"></a><span data-ttu-id="c7583-103">關於筆刷</span><span class="sxs-lookup"><span data-stu-id="c7583-103">About Brushes</span></span>

<span data-ttu-id="c7583-104">有兩種類型的筆刷：邏輯和實體。</span><span class="sxs-lookup"><span data-stu-id="c7583-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="c7583-105">*邏輯筆刷* 是應用程式用來繪製圖案的理想點陣圖描述。</span><span class="sxs-lookup"><span data-stu-id="c7583-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="c7583-106">*實體筆刷* 是設備磁碟機根據應用程式的邏輯筆刷定義所建立的實際點陣圖。</span><span class="sxs-lookup"><span data-stu-id="c7583-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="c7583-107">如需點陣圖的詳細資訊，請參閱 [點陣圖](bitmaps.md)。</span><span class="sxs-lookup"><span data-stu-id="c7583-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="c7583-108">當應用程式呼叫其中一個建立筆刷的函式時，它會抓取一個控點來識別邏輯筆刷。</span><span class="sxs-lookup"><span data-stu-id="c7583-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="c7583-109">當應用程式將此控制碼傳遞至 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式時，對應的顯示或印表機的設備磁碟機會建立實體筆刷。</span><span class="sxs-lookup"><span data-stu-id="c7583-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="c7583-110">下列主題描述筆刷：</span><span class="sxs-lookup"><span data-stu-id="c7583-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="c7583-111">筆刷來源</span><span class="sxs-lookup"><span data-stu-id="c7583-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="c7583-112">邏輯筆刷類型</span><span class="sxs-lookup"><span data-stu-id="c7583-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="c7583-113">模式區塊傳輸</span><span class="sxs-lookup"><span data-stu-id="c7583-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="c7583-114">啟用 ICM 的筆刷函數</span><span class="sxs-lookup"><span data-stu-id="c7583-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



