---
description: CSystemClock 類別會執行傳回系統時間的時鐘。
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: CSystemClock 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568033"
---
# <a name="csystemclock-class"></a><span data-ttu-id="a4aa6-103">CSystemClock 類別</span><span class="sxs-lookup"><span data-stu-id="a4aa6-103">CSystemClock class</span></span>

![csystemclock 類別階層](images/sclock01.png)

<span data-ttu-id="a4aa6-105">`CSystemClock`類別會執行傳回系統時間的時鐘。</span><span class="sxs-lookup"><span data-stu-id="a4aa6-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="a4aa6-106">這個類別衍生自 [**CBaseReferenceClock**](cbasereferenceclock.md) 類別，並新增 **IPersist** 和 [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) 介面的支援。</span><span class="sxs-lookup"><span data-stu-id="a4aa6-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="a4aa6-107">公用方法</span><span class="sxs-lookup"><span data-stu-id="a4aa6-107">Public Methods</span></span>                                        | <span data-ttu-id="a4aa6-108">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa6-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="a4aa6-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="a4aa6-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="a4aa6-110">建立這個物件的新執行個體。</span><span class="sxs-lookup"><span data-stu-id="a4aa6-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="a4aa6-111">**CSystemClock**</span><span class="sxs-lookup"><span data-stu-id="a4aa6-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="a4aa6-112">函式方法。</span><span class="sxs-lookup"><span data-stu-id="a4aa6-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="a4aa6-113">IAMClockAdjust 方法</span><span class="sxs-lookup"><span data-stu-id="a4aa6-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="a4aa6-114">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa6-114">Description</span></span>                                         |
| [<span data-ttu-id="a4aa6-115">**SetClockDelta**</span><span class="sxs-lookup"><span data-stu-id="a4aa6-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="a4aa6-116">調整時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="a4aa6-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="a4aa6-117">IPersist 方法</span><span class="sxs-lookup"><span data-stu-id="a4aa6-117">IPersist Methods</span></span>                                      | <span data-ttu-id="a4aa6-118">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa6-118">Description</span></span>                                         |
| [<span data-ttu-id="a4aa6-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="a4aa6-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="a4aa6-120">傳回物件 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4aa6-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



