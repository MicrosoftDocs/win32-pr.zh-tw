---
title: 取得系統時間
description: 取得系統時間
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- 多媒體計時器，系統時間
- 計時器，系統時間
- 系統時間
- timeGetTime 函式
- timeGetSystemTime 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462996"
---
# <a name="obtaining-the-system-time"></a><span data-ttu-id="72227-108">取得系統時間</span><span class="sxs-lookup"><span data-stu-id="72227-108">Obtaining the System Time</span></span>

<span data-ttu-id="72227-109">通常，在應用程式開始使用多媒體計時器服務之前，它會先抓取目前的 *系統時間*。</span><span class="sxs-lookup"><span data-stu-id="72227-109">Typically, before an application begins using the multimedia timer services, it retrieves the current *system time*.</span></span> <span data-ttu-id="72227-110">系統時間是自 Microsoft Windows 作業系統啟動以來的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="72227-110">The system time is the time, in milliseconds, since the Microsoft Windows operating system was started.</span></span> <span data-ttu-id="72227-111">您可以使用 [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) 或 [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) 函數來取得系統時間。</span><span class="sxs-lookup"><span data-stu-id="72227-111">You can use the [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) or [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) function to retrieve the system time.</span></span> <span data-ttu-id="72227-112">這兩個函數非常類似： **timeGetTime** 會傳回系統時間，而 **timeGetSystemTime** 會以系統時間填滿 [**MMTIME**](/previous-versions//dd757347(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="72227-112">These two functions are very similar: **timeGetTime** returns the system time, and **timeGetSystemTime** fills an [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure with the system time.</span></span>

 

 