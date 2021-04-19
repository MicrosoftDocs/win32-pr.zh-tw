---
description: 鎖定資源表示將 CPU 存取權授與儲存體。
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: " (Direct3D 9) 的鎖定資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973350"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="4f4b4-103"> (Direct3D 9) 的鎖定資源</span><span class="sxs-lookup"><span data-stu-id="4f4b4-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="4f4b4-104">鎖定資源表示將 CPU 存取權授與儲存體。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="4f4b4-105">下列為資源定義的鎖定選項：</span><span class="sxs-lookup"><span data-stu-id="4f4b4-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="4f4b4-106">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="4f4b4-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="4f4b4-107">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="4f4b4-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="4f4b4-108">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="4f4b4-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="4f4b4-109">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="4f4b4-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="4f4b4-110">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="4f4b4-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="4f4b4-111">如需鎖定旗標以及這些旗標如何與特定資源相關的詳細資訊，請參閱個別資源鎖定方法上的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="4f4b4-112">應用程式開發人員應該要注意的是，D3DLOCK \_ 捨棄、D3DLOCK \_ READONLY 和 D3DLOCK \_ NOOVERWRITE 旗標只是提示。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="4f4b4-113">執行時間不會檢查應用程式是否遵循這些旗標所指定的功能。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="4f4b4-114">指定 D3DLOCK \_ READONLY 但接著寫入資源的應用程式應該會預期未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="4f4b4-115">一般情況下，不保證會在較新版本中使用鎖定旗標（包括鎖定使用旗標），而且可能會產生顯著的效能影響。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="4f4b4-116">鎖定作業接著是解除鎖定作業。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="4f4b4-117">例如，在鎖定材質之後，應用程式會透過解除鎖定來會讓出直接存取鎖定的材質。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="4f4b4-118">除了授與處理器存取權之外，任何其他牽涉到該資源的作業都會在鎖定期間進行序列化。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="4f4b4-119">即使是針對非重迭的區域，也只允許資源的單一鎖定，而且在該介面上的鎖定作業未完成時，介面上沒有任何加速器作業可以進行。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="4f4b4-120">每個資源介面都有方法可鎖定包含的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="4f4b4-121">每個材質資源也可以鎖定該資源的子部分。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="4f4b4-122">2D 資源 (表面) 允許鎖定子矩形，而磁片區資源允許鎖定子磁片區或方塊。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="4f4b4-123">每個鎖定方法都會傳回一個結構，其中包含支援資源的儲存體指標，以及表示資料列或資料平面之間距離的值（視資源類型而定）。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="4f4b4-124">如需詳細資訊，請參閱資源介面的方法清單。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="4f4b4-125">傳回的指標一律指向鎖定子領域中的左上角位元組。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="4f4b4-126">使用索引和頂點緩衝區時，您可以進行多次鎖定呼叫;不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="4f4b4-127">DXTn 會將圖元儲存在編碼的4x4 區塊中，而且只能在4x4 界限上鎖定。</span><span class="sxs-lookup"><span data-stu-id="4f4b4-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f4b4-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f4b4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f4b4-129">Direct3D 資源</span><span class="sxs-lookup"><span data-stu-id="4f4b4-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



