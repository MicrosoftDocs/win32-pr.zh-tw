---
description: 有幾個網路提供者函式會採用緩衝區的位址和大小，而函式會將變數大小的資料結構放在其中。
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: 處理緩衝的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194079"
---
# <a name="handling-buffered-data"></a><span data-ttu-id="a0227-103">處理緩衝的資料</span><span class="sxs-lookup"><span data-stu-id="a0227-103">Handling Buffered Data</span></span>

<span data-ttu-id="a0227-104">有幾個網路提供者函式會採用緩衝區的位址和大小，而函式會將變數大小的資料結構放在其中。</span><span class="sxs-lookup"><span data-stu-id="a0227-104">Several of the network provider functions take the address and size of a buffer into which the function places a variable-sized data structure.</span></span>

<span data-ttu-id="a0227-105">在每個案例中，使用的機制都相同。</span><span class="sxs-lookup"><span data-stu-id="a0227-105">In each case, the mechanism used is the same.</span></span> <span data-ttu-id="a0227-106">呼叫端會配置緩衝區，並將其位址傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="a0227-106">The caller allocates a buffer and passes its address to the function.</span></span> <span data-ttu-id="a0227-107">它也會傳遞指定緩衝區大小的 **DWORD** 位址（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0227-107">It also passes the address of a **DWORD** that specifies the size of the buffer, in bytes.</span></span>

<span data-ttu-id="a0227-108">然後，此函式會將所要求的資料結構盡可能複製到緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="a0227-108">The function then copies as much of the requested data structure as it can into the buffer.</span></span> <span data-ttu-id="a0227-109">如果所有資料都符合緩衝區，此函式會傳回 WN \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="a0227-109">If all of the data fits into the buffer, the function returns WN\_SUCCESS.</span></span> <span data-ttu-id="a0227-110">如果資料不符合緩衝區，資料可能會保持不完整，且函式會設定 WN \_ 更多的 \_ 資料錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0227-110">If the data does not fit into the buffer, the data may be left incomplete, and the function sets the WN\_MORE\_DATA error.</span></span> <span data-ttu-id="a0227-111">在任一種情況下，表示緩衝區大小的 **DWORD** 會設定為資料結構實際需要的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a0227-111">In either case, the **DWORD** indicating the size of the buffer is set to the number of bytes actually required by the data structure.</span></span> <span data-ttu-id="a0227-112">如此一來，如果傳入的緩衝區太小，且函式失敗，則呼叫端可能會配置所需大小的新緩衝區，並再次呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="a0227-112">This way, if the buffer passed in was too small and the function failed, the caller may allocate a new buffer of the required size and call the function again.</span></span>

<span data-ttu-id="a0227-113">當傳回的資料結構包含可變長度的字串時，個別的資料結構通常會包含這些字串的指標。</span><span class="sxs-lookup"><span data-stu-id="a0227-113">When the data structures returned include variable-length strings, the individual data structures typically contain pointers to these strings.</span></span> <span data-ttu-id="a0227-114">字串本身也應放置在緩衝區內。</span><span class="sxs-lookup"><span data-stu-id="a0227-114">The strings themselves should also be placed within the buffer.</span></span> <span data-ttu-id="a0227-115">不過，請務必將它們放在緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="a0227-115">However, it is important to place them at the end of the buffer.</span></span> <span data-ttu-id="a0227-116">否則，它們會讓第 n 個結構的索引不可能發生。</span><span class="sxs-lookup"><span data-stu-id="a0227-116">Otherwise, they will make indexing to the Nth structure impossible.</span></span> <span data-ttu-id="a0227-117">換句話說，所有結構都是在緩衝區的開頭連續找出。</span><span class="sxs-lookup"><span data-stu-id="a0227-117">In other words, all structures are located contiguously at the beginning of the buffer.</span></span> <span data-ttu-id="a0227-118">字串或變數長度資料的指標必須是實際指標，而不是緩衝區的位移。</span><span class="sxs-lookup"><span data-stu-id="a0227-118">Pointers to strings or variable length data must be actual pointers, not offsets into the buffer.</span></span>

<span data-ttu-id="a0227-119">當緩衝區用來傳入並傳回只包含字串的資料時，指定緩衝區大小的 **DWORD** 應該設定為這些字串中的總字元數，而不是位元組數。</span><span class="sxs-lookup"><span data-stu-id="a0227-119">When a buffer is used to pass in and return data that consists only of strings, the **DWORD** specifying the size of the buffer should be set to the total number of characters that will fit in these strings, not to the number of bytes.</span></span>

 

 



