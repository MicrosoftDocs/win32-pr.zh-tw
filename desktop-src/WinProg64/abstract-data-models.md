---
title: 抽象資料模型
description: 每個應用程式和每個作業系統都有一個抽象資料模型。
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- 抽象資料模型64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bfb116d5afccba1b1ce3438f8b7135d01bc1b7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "107001067"
---
# <a name="abstract-data-models"></a><span data-ttu-id="26983-104">抽象資料模型</span><span class="sxs-lookup"><span data-stu-id="26983-104">Abstract Data Models</span></span>

<span data-ttu-id="26983-105">每個應用程式和每個作業系統都有一個抽象資料模型。</span><span class="sxs-lookup"><span data-stu-id="26983-105">Every application and every operating system has an abstract data model.</span></span> <span data-ttu-id="26983-106">許多應用程式不會明確地公開此資料模型，但模型會引導應用程式撰寫程式碼的方式。</span><span class="sxs-lookup"><span data-stu-id="26983-106">Many applications do not explicitly expose this data model, but the model guides the way in which the application's code is written.</span></span> <span data-ttu-id="26983-107">在32位程式設計模型中 (稱為 ILP32 模型) 、整數、long 和指標資料類型的長度是32位。</span><span class="sxs-lookup"><span data-stu-id="26983-107">In the 32-bit programming model (known as the ILP32 model), integer, long, and pointer data types are 32 bits in length.</span></span> <span data-ttu-id="26983-108">大部分的開發人員都已使用此模型，而不會加以實現。</span><span class="sxs-lookup"><span data-stu-id="26983-108">Most developers have used this model without realizing it.</span></span> <span data-ttu-id="26983-109">針對 WIN32 API 的歷程記錄，這是有效的 (但不一定是安全的) 假設要進行。</span><span class="sxs-lookup"><span data-stu-id="26983-109">For the history of the Win32 API, this has been a valid (although not necessarily safe) assumption to make.</span></span>

<span data-ttu-id="26983-110">在 64-bitWindows 中，這種資料類型大小的同位假設是不正確。</span><span class="sxs-lookup"><span data-stu-id="26983-110">In 64-bitWindows, this assumption of parity in data type sizes is invalid.</span></span> <span data-ttu-id="26983-111">因為大部分的應用程式不需要增加大小，所以將所有資料類型的長度設為64位將會浪費空間。</span><span class="sxs-lookup"><span data-stu-id="26983-111">Making all data types 64 bits in length would waste space, because most applications do not need the increased size.</span></span> <span data-ttu-id="26983-112">不過，應用程式確實需要64位資料的指標，而且需要在選取的案例中具有64位資料類型的能力。</span><span class="sxs-lookup"><span data-stu-id="26983-112">However, applications do need pointers to 64-bit data, and they need the ability to have 64-bit data types in selected cases.</span></span> <span data-ttu-id="26983-113">這些考慮會導致選取稱為 LLP64 (或 P64) 的抽象資料模型。</span><span class="sxs-lookup"><span data-stu-id="26983-113">These considerations led to the selection of an abstract data model called LLP64 (or P64).</span></span> <span data-ttu-id="26983-114">在 LLP64 資料模型中，只會展開指向64位的指標;所有其他基本資料類型 (整數和 long) 會維持32位的長度。</span><span class="sxs-lookup"><span data-stu-id="26983-114">In the LLP64 data model, only pointers expand to 64 bits; all other basic data types (integer and long) remain 32 bits in length.</span></span>

<span data-ttu-id="26983-115">一開始，在64位 Windows 上執行的大部分應用程式都是從32位 Windows 進行移植。</span><span class="sxs-lookup"><span data-stu-id="26983-115">Initially, most applications that run on 64-bit Windows will have been ported from 32-bit Windows.</span></span> <span data-ttu-id="26983-116">您必須在32和64位的 Windows 上執行相同來源（謹慎撰寫）的目標。</span><span class="sxs-lookup"><span data-stu-id="26983-116">It is a goal that the same source, carefully written, should run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="26983-117">定義資料模型並不會讓這項工作變得更容易。</span><span class="sxs-lookup"><span data-stu-id="26983-117">Defining the data model does not make this task easier.</span></span> <span data-ttu-id="26983-118">不過，確保資料模型只會影響指標資料類型是第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="26983-118">However, ensuring that the data model affects only pointer data types is the first step.</span></span> <span data-ttu-id="26983-119">第二個步驟是定義一組新的資料類型，讓開發人員自動調整其指標相關資料的大小。</span><span class="sxs-lookup"><span data-stu-id="26983-119">The second step is to define a set of new data types that allow developers to automatically size their pointer-related data.</span></span> <span data-ttu-id="26983-120">這可讓指標大小從32位變更為64位時，與指標相關聯的資料變更大小。</span><span class="sxs-lookup"><span data-stu-id="26983-120">This allows data associated with pointers to change size as the pointer size changes from 32 bits to 64 bits.</span></span> <span data-ttu-id="26983-121">基本資料類型的長度會維持32位，因此不會變更磁片上的資料大小、透過網路共用的資料，或是透過記憶體對應檔案共用的資料。</span><span class="sxs-lookup"><span data-stu-id="26983-121">Basic data types remain 32 bits in length, so there is no change in the size of data on the disk, data shared over a network, or data shared through memory-mapped files.</span></span> <span data-ttu-id="26983-122">這讓開發人員能夠輕鬆地將32位程式碼移植到64位 Windows。</span><span class="sxs-lookup"><span data-stu-id="26983-122">This relieves developers of much of the effort involved in porting 32-bit code to 64-bit Windows.</span></span>

<span data-ttu-id="26983-123">這些新的資料類型已新增至 Windows API 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="26983-123">These new data types have been added to the Windows API header files.</span></span> <span data-ttu-id="26983-124">因此，您現在可以開始使用新的類型。</span><span class="sxs-lookup"><span data-stu-id="26983-124">Therefore, you can start using the new types now.</span></span> <span data-ttu-id="26983-125">如需詳細資訊，請參閱 [新的資料類型](the-new-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="26983-125">For more information, see [The New Data Types](the-new-data-types.md).</span></span>

 

 




