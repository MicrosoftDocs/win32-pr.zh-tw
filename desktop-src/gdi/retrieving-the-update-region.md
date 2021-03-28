---
description: GetUpdateRect 和 GetUpdateRgn 函式會取出視窗的目前更新區域。
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: 正在抓取更新區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191916"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="02070-103">正在抓取更新區域</span><span class="sxs-lookup"><span data-stu-id="02070-103">Retrieving the Update Region</span></span>

<span data-ttu-id="02070-104">[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)和 [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)函式會取出視窗的目前更新區域。</span><span class="sxs-lookup"><span data-stu-id="02070-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="02070-105">GetUpdateRect 會) 括住整個更新區域的邏輯座標 (抓取最小的矩形。</span><span class="sxs-lookup"><span data-stu-id="02070-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="02070-106">GetUpdateRgn 會捕獲更新區域本身。</span><span class="sxs-lookup"><span data-stu-id="02070-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="02070-107">這些函式可用來計算更新區域的目前大小，以決定要執行繪圖作業的位置。</span><span class="sxs-lookup"><span data-stu-id="02070-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="02070-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)也會抓取封閉目前更新區域之最小矩形的維度，將維度複製到 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)結構中的 **rcPaint** 成員。</span><span class="sxs-lookup"><span data-stu-id="02070-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="02070-109">因為 **BeginPaint** 會驗證更新區域，所以在呼叫 **BeginPaint** 之後立即呼叫 [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)和 [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)會傳回空的更新區域。</span><span class="sxs-lookup"><span data-stu-id="02070-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



