---
description: 應用程式必須為此資料配置記憶體;TAPI 和服務提供者會提供資料。 如果作業是非同步，則在非同步回復訊息表示成功之前，無法使用資料。
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: 記憶體配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970129"
---
# <a name="memory-allocation"></a><span data-ttu-id="5e659-104">記憶體配置</span><span class="sxs-lookup"><span data-stu-id="5e659-104">Memory Allocation</span></span>

<span data-ttu-id="5e659-105">應用程式必須為此資料配置記憶體;TAPI 和服務提供者會提供資料。</span><span class="sxs-lookup"><span data-stu-id="5e659-105">Applications must allocate memory for this data; TAPI and the service provider provide the data.</span></span> <span data-ttu-id="5e659-106">如果作業是非同步，則在非同步回復訊息表示成功之前，無法使用資料。</span><span class="sxs-lookup"><span data-stu-id="5e659-106">If the operation is asynchronous, the data is not available until the asynchronous reply message indicates success.</span></span>

<span data-ttu-id="5e659-107">用來在應用程式與 TAPI 之間傳遞資料的所有資料結構都會 *壓平* 合併。</span><span class="sxs-lookup"><span data-stu-id="5e659-107">All data structures used to pass data between the application and the TAPI are *flattened*.</span></span> <span data-ttu-id="5e659-108">也就是說，資料結構不包含子結構的指標，其中包含大小可變大小的資料元件。</span><span class="sxs-lookup"><span data-stu-id="5e659-108">That is, data structures do not contain pointers to substructures that contain variably sized data components.</span></span> <span data-ttu-id="5e659-109">相反地，用來將可變數據量傳回給應用程式的資料結構必須具有下列中繼架構：</span><span class="sxs-lookup"><span data-stu-id="5e659-109">Instead, data structures used to pass variable amounts of data back to the application must have the following metastructure:</span></span>

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

<span data-ttu-id="5e659-110">**DwTotalSize** 成員是配置給此資料結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e659-110">The **dwTotalSize** member is the size, in bytes, allocated to this data structure.</span></span> <span data-ttu-id="5e659-111">它會標示資料結構的結尾，並由應用程式設定，然後再叫用使用此資料結構的函數。</span><span class="sxs-lookup"><span data-stu-id="5e659-111">It marks the end of the data structure and is set by the application before it invokes the function that uses this data structure.</span></span> <span data-ttu-id="5e659-112">函式不會讀取或寫入超過此大小。</span><span class="sxs-lookup"><span data-stu-id="5e659-112">The function does not read or write beyond this size.</span></span> <span data-ttu-id="5e659-113">應用程式必須設定 **dwTotalSize** 成員，以表示配置給 TAPI 的總位元組數，以傳回結構的內容。</span><span class="sxs-lookup"><span data-stu-id="5e659-113">An application must set the **dwTotalSize** member to indicate the total number of bytes allocated for TAPI to return the contents of the structure.</span></span>

<span data-ttu-id="5e659-114">TAPI 會填入 **dwNeededSize** 成員。</span><span class="sxs-lookup"><span data-stu-id="5e659-114">TAPI fills in the **dwNeededSize** member.</span></span> <span data-ttu-id="5e659-115">它會指出需要多少位元組才能傳回所有要求的資料。</span><span class="sxs-lookup"><span data-stu-id="5e659-115">It indicates how many bytes are required to return all the requested data.</span></span> <span data-ttu-id="5e659-116">大小可變大小欄位的存在通常會讓應用程式無法估計配置所需的資料結構大小。</span><span class="sxs-lookup"><span data-stu-id="5e659-116">The existence of variably sized fields often makes it impossible for the application to estimate the data structure size required to allocate.</span></span> <span data-ttu-id="5e659-117">這個欄位會傳回資料實際所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5e659-117">This field returns the number of bytes actually required for the data.</span></span> <span data-ttu-id="5e659-118">這個數位可能小於、等於或大於 **dwTotalSize**，而且會包含 **dwTotalSize** 成員本身的空間。</span><span class="sxs-lookup"><span data-stu-id="5e659-118">This number could be smaller than, equal to, or larger than **dwTotalSize**, and it includes space for the **dwTotalSize** member itself.</span></span> <span data-ttu-id="5e659-119">如果較大，則只會部分填滿傳回的結構。</span><span class="sxs-lookup"><span data-stu-id="5e659-119">If larger, the returned structure is only partially filled.</span></span> <span data-ttu-id="5e659-120">如果部分結構中有應用程式所需的欄位，就不需要執行任何其他動作。</span><span class="sxs-lookup"><span data-stu-id="5e659-120">If the fields the application requires are available in the partial structure, nothing else must be done.</span></span> <span data-ttu-id="5e659-121">否則，應用程式應至少配置 **dwNeededSize** 大小的結構，然後再次叫用函式。</span><span class="sxs-lookup"><span data-stu-id="5e659-121">Otherwise, the application should allocate a structure at least the size of **dwNeededSize** and invoke the function again.</span></span> <span data-ttu-id="5e659-122">通常，您可以使用足夠的空間來傳回所有資訊，雖然可能會再次增加大小。</span><span class="sxs-lookup"><span data-stu-id="5e659-122">Usually, enough space is available this time to return all the information, although it is possible the size could have increased again.</span></span>

<span data-ttu-id="5e659-123">如果 TAPI 將資料傳回給應用程式，則會填滿 **dwUsedSize** 成員，以表示包含有用資料之資料結構部分的實際大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e659-123">TAPI fills the **dwUsedSize** member if it returns data to the application to indicate the actual size, in bytes, of the portion of the data structure that contains useful data.</span></span> <span data-ttu-id="5e659-124">舉例來說，如果配置的結構太小，而截斷的欄位是大小可變大小的欄位，則 **dwNeededSize** 大於 **dwTotalSize**，且截斷的欄位會保留空白。</span><span class="sxs-lookup"><span data-stu-id="5e659-124">If, for example, a structure that was allocated was too small and the truncated field is a variably sized field, **dwNeededSize** is larger than **dwTotalSize**, and the truncated field is left empty.</span></span> <span data-ttu-id="5e659-125">因此， **dwUsedSize** 成員可能小於 **dwTotalSize**。</span><span class="sxs-lookup"><span data-stu-id="5e659-125">The **dwUsedSize** member could therefore be smaller than **dwTotalSize**.</span></span> <span data-ttu-id="5e659-126">部分域值不會傳回。</span><span class="sxs-lookup"><span data-stu-id="5e659-126">Partial field values are not returned.</span></span>

<span data-ttu-id="5e659-127">遵循此標頭是資料結構的固定部分。</span><span class="sxs-lookup"><span data-stu-id="5e659-127">Following this header is the fixed part of the data structure.</span></span> <span data-ttu-id="5e659-128">它包含一般欄位和大小/位移組，以描述實際的大小可變大小欄位。</span><span class="sxs-lookup"><span data-stu-id="5e659-128">It contains regular fields and size/offset pairs that describe the actual variably sized fields.</span></span> <span data-ttu-id="5e659-129">[位移] 欄位包含從記錄開頭大小可變大小欄位的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e659-129">The offset field contains the offset in bytes of the variably sized field from the beginning of the record.</span></span> <span data-ttu-id="5e659-130">[大小] 欄位包含大小可變大小欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e659-130">The size field contains the size in bytes of the variably sized field.</span></span> <span data-ttu-id="5e659-131">如果 [大小可變大小] 欄位是空的，則 [大小] 欄位為零，而且位移設定為零。</span><span class="sxs-lookup"><span data-stu-id="5e659-131">If a variably sized field is empty, then the size field is zero and the offset is set to zero.</span></span> <span data-ttu-id="5e659-132">大小可變已調整大小的欄位如果總結構大小不足，則會被截斷。</span><span class="sxs-lookup"><span data-stu-id="5e659-132">Variably sized fields that would be truncated if the total structure size is insufficient are left empty.</span></span> <span data-ttu-id="5e659-133">也就是說，其 size 欄位設定為零，而且位移設定為零。</span><span class="sxs-lookup"><span data-stu-id="5e659-133">That is, their size field is set to zero and the offset is set to zero.</span></span> <span data-ttu-id="5e659-134">大小可變大小的欄位會在固定欄位之後。</span><span class="sxs-lookup"><span data-stu-id="5e659-134">The variably sized fields follow the fixed fields.</span></span>

<span data-ttu-id="5e659-135">如果服務提供者必須填入變數成員，TAPI 會將對應的大小和位移成員初始化為零。</span><span class="sxs-lookup"><span data-stu-id="5e659-135">If the service provider must fill a variable member, TAPI initializes the corresponding size and offset members to zero.</span></span> <span data-ttu-id="5e659-136">如果服務提供者填滿變數成員，它就必須將對應的大小和位移成員設定為適當的值，包括 **dwUsedSize** 和 **dwNeededSize** （如果設定變數成員的話）。</span><span class="sxs-lookup"><span data-stu-id="5e659-136">If the service provider fills in the variable member, it must set the corresponding size and offset members to appropriate values, including **dwUsedSize** and **dwNeededSize** if it sets variable members.</span></span> <span data-ttu-id="5e659-137">服務提供者不得截斷變數成員，使其符合可用的空間。</span><span class="sxs-lookup"><span data-stu-id="5e659-137">The service provider must not truncate a variable member to make it fit into the available space.</span></span>

<span data-ttu-id="5e659-138">服務提供者必須在結構的固定成員之後立即啟動變數成員，並且在配置的記憶體結尾留下任何額外的空間，讓 TAPI 可將它用於可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="5e659-138">The service provider must start variable members immediately after the fixed members of the structure, and leave any extra space at the end of the allocated memory so that TAPI can use it for the variable-length members.</span></span> <span data-ttu-id="5e659-139">它可以依任何順序放置變數成員，但成員必須是連續的。</span><span class="sxs-lookup"><span data-stu-id="5e659-139">It can place the variable members in any order, but the members must be contiguous.</span></span>

 

 



