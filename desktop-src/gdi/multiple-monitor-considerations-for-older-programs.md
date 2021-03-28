---
description: 一般而言，較舊的應用程式不需要在多個監視系統上進行變更。
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: 舊版程式的多個監視器考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972633"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="81e70-103">舊版程式的多個監視器考慮</span><span class="sxs-lookup"><span data-stu-id="81e70-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="81e70-104">一般而言，較舊的應用程式不需要在多個監視系統上進行變更。</span><span class="sxs-lookup"><span data-stu-id="81e70-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="81e70-105">大部分的情況下，系統看起來只有一個顯示器。</span><span class="sxs-lookup"><span data-stu-id="81e70-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="81e70-106">系統計量會反映主顯示器和全螢幕應用程式會顯示在主要畫面上。</span><span class="sxs-lookup"><span data-stu-id="81e70-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="81e70-107">系統會處理最小化、maximization、功能表和對話方塊。</span><span class="sxs-lookup"><span data-stu-id="81e70-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="81e70-108">不過，某些程式會有問題。</span><span class="sxs-lookup"><span data-stu-id="81e70-108">However, some programs will have problems.</span></span> <span data-ttu-id="81e70-109">有些可能發生問題的部分是遠端控制應用程式、具有直接硬體存取的應用程式，以及已修補 GDI 或顯示驅動程式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="81e70-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="81e70-110">在這些情況下，使用者可能需要停用主要監視器以外的任何監視。</span><span class="sxs-lookup"><span data-stu-id="81e70-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



