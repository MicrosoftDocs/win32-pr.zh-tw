---
description: 當使用大小可變大小的資料結構來傳送 TAPI 和應用程式之間的資訊時，應用程式會負責配置所需的記憶體。
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: 大小可變大小的資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194495"
---
# <a name="variably-sized-data-structures"></a><span data-ttu-id="5c172-103">大小可變大小的資料結構</span><span class="sxs-lookup"><span data-stu-id="5c172-103">Variably Sized Data Structures</span></span>

<span data-ttu-id="5c172-104">當使用大小可變大小的資料結構來傳送 TAPI 和應用程式之間的資訊時，應用程式會負責配置所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5c172-104">When variably sized data structures are used to transmit information between TAPI and the application, the application is responsible for allocating the necessary memory.</span></span> <span data-ttu-id="5c172-105">配置的記憶體數量至少必須夠大，才能用於資料結構的固定部分，而且是由應用程式在資料結構的 **dwTotalSize** 成員中設定。</span><span class="sxs-lookup"><span data-stu-id="5c172-105">The amount of memory allocated must be at least large enough for the fixed portion of the data structure, and is set by the application in the **dwTotalSize** member of the data structure.</span></span> <span data-ttu-id="5c172-106">**DwUsedSize** 和 **dwNeededSize** 成員是由 TAPI 填入。</span><span class="sxs-lookup"><span data-stu-id="5c172-106">The **dwUsedSize** and **dwNeededSize** members are filled in by TAPI.</span></span> <span data-ttu-id="5c172-107">如果 **dwTotalSize** 小於固定部分的大小，則會傳回 LINEERR/PHONEERR \_ STRUCTURETOOSMALL。</span><span class="sxs-lookup"><span data-stu-id="5c172-107">If **dwTotalSize** is less than the size of the fixed portion, then LINEERR/ PHONEERR\_STRUCTURETOOSMALL is returned.</span></span> <span data-ttu-id="5c172-108">如果函數傳回成功，則會填入固定部分中的所有欄位。</span><span class="sxs-lookup"><span data-stu-id="5c172-108">If a function returns success, then all the fields in the fixed portion have been filled in.</span></span> <span data-ttu-id="5c172-109">**DwUsedSize** 和 **dwNeededSize** 成員可以進行比較，以判斷是否已填入所有變數部分，以及需要多少空間來填滿它們。</span><span class="sxs-lookup"><span data-stu-id="5c172-109">The **dwUsedSize** and **dwNeededSize** members can be compared to determine if all variable parts have been filled in, and how much space would be required to fill them all in.</span></span>

<span data-ttu-id="5c172-110">如果 **dwNeededSize** 等於 **dwUsedSize**，則會填入所有固定和變數部分。</span><span class="sxs-lookup"><span data-stu-id="5c172-110">If **dwNeededSize** is equal to **dwUsedSize**, then all fixed and variable parts have been filled in.</span></span> <span data-ttu-id="5c172-111">如果 **dwNeededSize** 大於 **dwUsedSize**，某些變數部分可能已經填入，但已填滿的大小可變大小欄位就剛好未定義。</span><span class="sxs-lookup"><span data-stu-id="5c172-111">If **dwNeededSize** is larger than **dwUsedSize**, some variable parts may have been filled in, but exactly which variably sized fields have been filled in is undefined.</span></span> <span data-ttu-id="5c172-112">沒有任何變數部分會被截斷，而且因為空間不足而被截斷的變數部分，則會將兩個對應的「位移」和「大小」部分設為零來表示。</span><span class="sxs-lookup"><span data-stu-id="5c172-112">No variable part is ever truncated, and variable parts that would have been truncated due to insufficient space are indicated by having both of their corresponding "Offset" and "Size" parts set to zero.</span></span> <span data-ttu-id="5c172-113">如果這些都不是零 (且) 未傳回錯誤，則會指出有效、nontruncated 的變數部分資料的位移和大小。</span><span class="sxs-lookup"><span data-stu-id="5c172-113">If these are not both zero (and no error was returned), they indicate the offset and size of valid, nontruncated variable-part data.</span></span>

<span data-ttu-id="5c172-114">應用程式一律會配置並指出結構的 **dwNeededSize** 位元組，並再次呼叫 "Get" 函式，直到函式傳回 Success 且 **dwNeededSize** 等於 **dwUsedSize**，藉以保證會填入所有變數部分。</span><span class="sxs-lookup"><span data-stu-id="5c172-114">An application can always guarantee that all variable parts are filled in by allocating and indicating **dwNeededSize** bytes for the structure and calling the "Get" function again until the function returns success and **dwNeededSize** equals **dwUsedSize**.</span></span> <span data-ttu-id="5c172-115">這應該會在第二次嘗試時發生，但競爭情形會導致呼叫之間的變數部分大小變更，這應該是很罕見的情況。</span><span class="sxs-lookup"><span data-stu-id="5c172-115">This should happen on the second try except for race conditions that cause changes in the size of variable parts between calls, which should be a rare occurrence.</span></span>

> [!Note]  
> <span data-ttu-id="5c172-116">大小可變大小結構中的所有文字字串（無論編碼方式）都應該根據一般 C 字串處理慣例，以 **Null** 終止。</span><span class="sxs-lookup"><span data-stu-id="5c172-116">All text strings, regardless of encoding, in variably sized structures should be **NULL**-terminated according to normal C string-handling conventions.</span></span>

 

 

 



