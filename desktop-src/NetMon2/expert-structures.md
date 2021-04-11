---
description: 網路監視器和一般 helper 函式所提供的專家協助程式函式會使用下表所述的結構。
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: 專家結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b9da00a71c3cdb9defe4396f4339f750cca359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936637"
---
# <a name="expert-structures"></a><span data-ttu-id="888a0-103">專家結構</span><span class="sxs-lookup"><span data-stu-id="888a0-103">Expert Structures</span></span>

<span data-ttu-id="888a0-104">網路監視器和一般 helper 函式所提供的專家協助程式函式會使用下表所述的結構。</span><span class="sxs-lookup"><span data-stu-id="888a0-104">Expert helper functions provided by Network Monitor and common helper functions use the structures described in the following table.</span></span>



| <span data-ttu-id="888a0-105">結構</span><span class="sxs-lookup"><span data-stu-id="888a0-105">Structure</span></span>                                              | <span data-ttu-id="888a0-106">Description</span><span class="sxs-lookup"><span data-stu-id="888a0-106">Description</span></span>                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="888a0-107">**CONFIGUREDEXPERT**</span><span class="sxs-lookup"><span data-stu-id="888a0-107">**CONFIGUREDEXPERT**</span></span>](configuredexpert.md)           | <span data-ttu-id="888a0-108">將專家 DLL 與其設定產生關聯。</span><span class="sxs-lookup"><span data-stu-id="888a0-108">Associates an expert DLL with its configuration.</span></span>                                                       |
| [<span data-ttu-id="888a0-109">**EXPERTCONFIG**</span><span class="sxs-lookup"><span data-stu-id="888a0-109">**EXPERTCONFIG**</span></span>](expertconfig.md)                   | <span data-ttu-id="888a0-110">提供原始的設定資料。</span><span class="sxs-lookup"><span data-stu-id="888a0-110">Provides raw configuration data.</span></span>                                                                       |
| [<span data-ttu-id="888a0-111">**EXPERTENUMINFO**</span><span class="sxs-lookup"><span data-stu-id="888a0-111">**EXPERTENUMINFO**</span></span>](expertenuminfo.md)               | <span data-ttu-id="888a0-112">提供專家 DLL 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="888a0-112">Provides information about the expert DLL.</span></span> <span data-ttu-id="888a0-113">網路監視器會使用資訊。</span><span class="sxs-lookup"><span data-stu-id="888a0-113">Network Monitor uses the information.</span></span>                       |
| [<span data-ttu-id="888a0-114">**EXPERTFRAMEDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="888a0-114">**EXPERTFRAMEDESCRIPTOR**</span></span>](expertframedescriptor.md) | <span data-ttu-id="888a0-115">提供框架的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="888a0-115">Provides information about a frame.</span></span>                                                                    |
| [<span data-ttu-id="888a0-116">**EXPERTSTARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="888a0-116">**EXPERTSTARTUPINFO**</span></span>](expertstartupinfo.md)         | <span data-ttu-id="888a0-117">提供專家的相關啟動資訊。</span><span class="sxs-lookup"><span data-stu-id="888a0-117">Provides startup information about the expert.</span></span>                                                         |
| [<span data-ttu-id="888a0-118">**EXPERTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="888a0-118">**EXPERTSTATUS**</span></span>](expertstatus.md)                   | <span data-ttu-id="888a0-119">提供正在執行之專家的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="888a0-119">Provides the current status of a running expert.</span></span>                                                       |
| [<span data-ttu-id="888a0-120">**FILTEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="888a0-120">**FILTEROBJECT**</span></span>](filterobject.md)                   | <span data-ttu-id="888a0-121">定義專家的顯示篩選特性。</span><span class="sxs-lookup"><span data-stu-id="888a0-121">Defines the display filter characteristics for an expert.</span></span>                                              |
| [<span data-ttu-id="888a0-122">**NMEVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="888a0-122">**NMEVENTDATA**</span></span>](nmeventdata.md)                     | <span data-ttu-id="888a0-123">提供專家檢視器中顯示的行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="888a0-123">Provides information about a line displayed in the expert viewer.</span></span>                                      |
| [<span data-ttu-id="888a0-124">**NMCOLUMNINFO**</span><span class="sxs-lookup"><span data-stu-id="888a0-124">**NMCOLUMNINFO**</span></span>](nmcolumninfo.md)                   | <span data-ttu-id="888a0-125">提供在事件檢視器中定義資料行的資訊。</span><span class="sxs-lookup"><span data-stu-id="888a0-125">Provides information that defines a column in the Event Viewer.</span></span>                                        |
| [<span data-ttu-id="888a0-126">**NMCOLUMNVARIANT**</span><span class="sxs-lookup"><span data-stu-id="888a0-126">**NMCOLUMNVARIANT**</span></span>](nmcolumnvariant.md)             | <span data-ttu-id="888a0-127">提供容器，讓所有可能的資料插入事件檢視器中一行的資料行。</span><span class="sxs-lookup"><span data-stu-id="888a0-127">Provides a container for all possible data inserted into a column on one line in the Event Viewer.</span></span>     |
| [<span data-ttu-id="888a0-128">**NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="888a0-128">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)                   | <span data-ttu-id="888a0-129">變數中的進入點，指出要使用聯集的哪個元素，以及如何將它格式化。</span><span class="sxs-lookup"><span data-stu-id="888a0-129">The entry point in the variant that indicates which element of the union to use, and how to format it.</span></span> |



 

<span data-ttu-id="888a0-130">網路監視器也提供 (helper 函式的匯出函式，專家可以呼叫) 和列舉。</span><span class="sxs-lookup"><span data-stu-id="888a0-130">Network Monitor also provides export functions (helper functions that the expert can call) and enumerations.</span></span>



| <span data-ttu-id="888a0-131">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="888a0-131">For information about</span></span>                                          | <span data-ttu-id="888a0-132">請參閱</span><span class="sxs-lookup"><span data-stu-id="888a0-132">See</span></span>                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="888a0-133">匯出函式，將進入點提供給您的專家 DLL。</span><span class="sxs-lookup"><span data-stu-id="888a0-133">Export Functions that provide entry points to your expert DLL.</span></span> | [<span data-ttu-id="888a0-134">專家 DLL 匯出函式</span><span class="sxs-lookup"><span data-stu-id="888a0-134">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="888a0-135">可由專家和剖析器呼叫的 Helper 函式。</span><span class="sxs-lookup"><span data-stu-id="888a0-135">Helper functions that can be called by experts and parsers.</span></span>    | [<span data-ttu-id="888a0-136">專家和剖析器一般函數</span><span class="sxs-lookup"><span data-stu-id="888a0-136">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="888a0-137">僅由專家呼叫的 Helper 函式。</span><span class="sxs-lookup"><span data-stu-id="888a0-137">Helper functions that are called only by experts.</span></span>              | [<span data-ttu-id="888a0-138">專家功能</span><span class="sxs-lookup"><span data-stu-id="888a0-138">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="888a0-139">專家結構和函數所使用的列舉。</span><span class="sxs-lookup"><span data-stu-id="888a0-139">Enumerations used by expert structures and functions.</span></span>          | [<span data-ttu-id="888a0-140">專家列舉</span><span class="sxs-lookup"><span data-stu-id="888a0-140">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 



