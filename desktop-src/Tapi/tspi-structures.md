---
description: TSPI 使用的資料結構與 TAPI 結構中所定義的結構相同，但 TUISPICREATEDIALOGINSTANCEPARAMS 除外。
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: TSPI 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985650"
---
# <a name="tspi-structures"></a><span data-ttu-id="b30c2-103">TSPI 結構</span><span class="sxs-lookup"><span data-stu-id="b30c2-103">TSPI Structures</span></span>

<span data-ttu-id="b30c2-104">TSPI 使用的資料結構與 [TAPI 結構](./tapi-structures.md)中所定義的結構相同，但 [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)除外。</span><span class="sxs-lookup"><span data-stu-id="b30c2-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="b30c2-105">如果是大部分較大型的資料結構，則填寫成員的責任會在服務提供者和 TAPI 之間劃分。</span><span class="sxs-lookup"><span data-stu-id="b30c2-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="b30c2-106">服務提供者必須保留出現在 TAPI 所擁有之成員的值。</span><span class="sxs-lookup"><span data-stu-id="b30c2-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="b30c2-107">服務提供者必須設定哪些成員的描述，而且必須保留這些成員的描述，會在參考該資料結構之函式的函數區段中提供。</span><span class="sxs-lookup"><span data-stu-id="b30c2-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="b30c2-108">針對每個結構，參考區段會列出下列專案：</span><span class="sxs-lookup"><span data-stu-id="b30c2-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="b30c2-109">結構的用途</span><span class="sxs-lookup"><span data-stu-id="b30c2-109">The purpose of the structure</span></span>
-   <span data-ttu-id="b30c2-110">值或欄位的描述</span><span class="sxs-lookup"><span data-stu-id="b30c2-110">A description of the values or fields</span></span>
-   <span data-ttu-id="b30c2-111">結構延伸的描述</span><span class="sxs-lookup"><span data-stu-id="b30c2-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="b30c2-112">使用結構的選擇性批註</span><span class="sxs-lookup"><span data-stu-id="b30c2-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="b30c2-113">其他函數、訊息、常數或結構的選擇性參考。</span><span class="sxs-lookup"><span data-stu-id="b30c2-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="b30c2-114">所有資料結構的記憶體（其表示由 TAPI 和服務提供者發佈並共用）都是由 TAPI 或使用 TAPI 的應用程式所配置。</span><span class="sxs-lookup"><span data-stu-id="b30c2-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="b30c2-115">TAPI 會將指標傳遞至 TSPI 函式，以傳回信息。</span><span class="sxs-lookup"><span data-stu-id="b30c2-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="b30c2-116">TSPI 會以所要求的資訊填入資料結構。</span><span class="sxs-lookup"><span data-stu-id="b30c2-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="b30c2-117">如果作業是非同步，則在非同步回復回呼表示成功之前，將無法使用該資訊。</span><span class="sxs-lookup"><span data-stu-id="b30c2-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="b30c2-118">某些結構包含大小和位移欄位，可在結構的變數部分中定義字串的位置和長度。</span><span class="sxs-lookup"><span data-stu-id="b30c2-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="b30c2-119">如果要求服務提供者加入字串，但沒有任何可用的字串，服務提供者必須以下列其中一種方式來指出這個狀況：</span><span class="sxs-lookup"><span data-stu-id="b30c2-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="b30c2-120">將 [大小] 和 [位移] 欄位設定為0。</span><span class="sxs-lookup"><span data-stu-id="b30c2-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="b30c2-121">將 [位移] 欄位設定為非零，但將大小設定為0。</span><span class="sxs-lookup"><span data-stu-id="b30c2-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="b30c2-122">將 Offset 欄位設定為非零、將大小設定為1，並將位移的位元組設定為0。</span><span class="sxs-lookup"><span data-stu-id="b30c2-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 
