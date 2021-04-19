---
description: 目前，呼叫的所有時間都是由應用程式所剩餘。
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: 撥號狀態計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972452"
---
# <a name="call-state-timer"></a><span data-ttu-id="160c7-103">撥號狀態計時器</span><span class="sxs-lookup"><span data-stu-id="160c7-103">Call State Timer</span></span>

<span data-ttu-id="160c7-104">目前，呼叫的所有時間都是由應用程式所剩餘。</span><span class="sxs-lookup"><span data-stu-id="160c7-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="160c7-105">如果應用程式監視大量的呼叫，而如果有多個應用程式存在（可能在多部伺服器上），則可能需要在相同的呼叫上維護計時器，才能讓這項工作變得很繁瑣。</span><span class="sxs-lookup"><span data-stu-id="160c7-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="160c7-106">因此，伺服器會處理撥號狀態的時間更有意義。</span><span class="sxs-lookup"><span data-stu-id="160c7-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="160c7-107">[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)中的 **tStateEntryTime** 成員允許回報狀態中的呼叫時間。</span><span class="sxs-lookup"><span data-stu-id="160c7-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="160c7-108">**SYSTIME** 類型的成員 () 表示輸入目前狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="160c7-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



