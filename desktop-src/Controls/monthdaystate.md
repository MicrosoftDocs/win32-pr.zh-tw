---
title: MONTHDAYSTATE
description: MONTHDAYSTATE 資料型別是保存每個月各天狀態的位位。
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839383"
---
# <a name="monthdaystate"></a><span data-ttu-id="39285-103">MONTHDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="39285-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="39285-104">MONTHDAYSTATE 資料型別是保存每個月各天狀態的位位。</span><span class="sxs-lookup"><span data-stu-id="39285-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="39285-105">資料類型定義于 Commctrl 中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="39285-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="39285-106">每個位 (0 到 30) 代表一個月中某一天的狀態。</span><span class="sxs-lookup"><span data-stu-id="39285-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="39285-107">如果位元是開啟的，則對應的日期會以粗體顯示；否則就不會強調其顯示。</span><span class="sxs-lookup"><span data-stu-id="39285-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="39285-108">這個資料類型會搭配 [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) 訊息和對應的宏 [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate)使用。</span><span class="sxs-lookup"><span data-stu-id="39285-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="39285-109">當使用 MONTHDAYSTATE 值來參考的月數少於31天時，只會存取所需的位。</span><span class="sxs-lookup"><span data-stu-id="39285-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="39285-110">此資料類型是在 Comctl32.dll [4.70 版](common-control-versions.md) 中第一次定義。</span><span class="sxs-lookup"><span data-stu-id="39285-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




