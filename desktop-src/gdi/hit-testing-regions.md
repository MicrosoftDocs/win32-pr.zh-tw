---
description: 應用程式會在區域上執行點擊測試，以判斷目前資料指標位置的座標。
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: 點擊測試區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191941"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="4fa7b-103">點擊測試區域</span><span class="sxs-lookup"><span data-stu-id="4fa7b-103">Hit Testing Regions</span></span>

<span data-ttu-id="4fa7b-104">應用程式會在區域上執行點擊測試，以判斷目前資料指標位置的座標。</span><span class="sxs-lookup"><span data-stu-id="4fa7b-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="4fa7b-105">然後，它會將這些座標和識別區域的控制碼傳遞給 [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) 函數。</span><span class="sxs-lookup"><span data-stu-id="4fa7b-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="4fa7b-106">您可以處理各種不同的滑鼠訊息（例如， [**wm \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) 、 [**wm \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) 、 [**wm \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) 和 [**wm \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md)）來抓取游標座標。</span><span class="sxs-lookup"><span data-stu-id="4fa7b-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="4fa7b-107">PtInRegion 的傳回值會指出游標位置是否在指定的區域內。</span><span class="sxs-lookup"><span data-stu-id="4fa7b-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
