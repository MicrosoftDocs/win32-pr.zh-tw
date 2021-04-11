---
description: 下列功能是專家 Dll 的進入點，以及作業系統和網路監視器的呼叫。
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: 專家 DLL 匯出函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936638"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="a4b90-103">專家 DLL 匯出函式</span><span class="sxs-lookup"><span data-stu-id="a4b90-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="a4b90-104">下列功能是專家 Dll 的進入點，以及作業系統和網路監視器的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a4b90-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="a4b90-105">函式</span><span class="sxs-lookup"><span data-stu-id="a4b90-105">Function</span></span>                                   | <span data-ttu-id="a4b90-106">描述</span><span class="sxs-lookup"><span data-stu-id="a4b90-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4b90-107">**DllMain 專家**</span><span class="sxs-lookup"><span data-stu-id="a4b90-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="a4b90-108">表示已載入或卸載專家 DLL。</span><span class="sxs-lookup"><span data-stu-id="a4b90-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="a4b90-109">當進程載入或卸載 DLL 時，作業系統會呼叫 [**DllMain**](/windows/desktop/Dlls/dllmain) 函數。</span><span class="sxs-lookup"><span data-stu-id="a4b90-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="a4b90-110">**註冊專家**</span><span class="sxs-lookup"><span data-stu-id="a4b90-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="a4b90-111">判斷有關 DLL 內專家的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="a4b90-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="a4b90-112">網路監視器會呼叫 **Register** 函數。</span><span class="sxs-lookup"><span data-stu-id="a4b90-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="a4b90-113">**設定**</span><span class="sxs-lookup"><span data-stu-id="a4b90-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="a4b90-114">設定 DLL 內的專家。</span><span class="sxs-lookup"><span data-stu-id="a4b90-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="a4b90-115">網路監視器會呼叫 [**Configure**](configure.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="a4b90-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="a4b90-116">**執行**</span><span class="sxs-lookup"><span data-stu-id="a4b90-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="a4b90-117">啟動 DLL 內的專家。</span><span class="sxs-lookup"><span data-stu-id="a4b90-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="a4b90-118">網路監視器會呼叫 [**Run**](run.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="a4b90-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="a4b90-119">網路監視器也提供專家可以呼叫的結構、列舉和 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="a4b90-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="a4b90-120">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="a4b90-120">For information about</span></span>                                      | <span data-ttu-id="a4b90-121">請參閱</span><span class="sxs-lookup"><span data-stu-id="a4b90-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a4b90-122">可由專家和剖析器呼叫的協助程式函數</span><span class="sxs-lookup"><span data-stu-id="a4b90-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="a4b90-123">專家和剖析器一般函數</span><span class="sxs-lookup"><span data-stu-id="a4b90-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="a4b90-124">僅由專家呼叫的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="a4b90-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="a4b90-125">專家功能</span><span class="sxs-lookup"><span data-stu-id="a4b90-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="a4b90-126">專家函式所使用的結構</span><span class="sxs-lookup"><span data-stu-id="a4b90-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="a4b90-127">專家結構</span><span class="sxs-lookup"><span data-stu-id="a4b90-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="a4b90-128">專家結構和函數所使用的列舉</span><span class="sxs-lookup"><span data-stu-id="a4b90-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="a4b90-129">專家列舉</span><span class="sxs-lookup"><span data-stu-id="a4b90-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
