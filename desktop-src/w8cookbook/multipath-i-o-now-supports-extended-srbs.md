---
title: 多重路徑 i/o 現在支援延伸儲存體要求區塊
description: 多重路徑 i/o 現在支援延伸儲存體要求區塊
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104316657"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a><span data-ttu-id="6fffa-103">多重路徑 i/o 現在支援延伸儲存體要求區塊</span><span class="sxs-lookup"><span data-stu-id="6fffa-103">Multipath I/O now supports extended storage request blocks</span></span>

## <a name="platforms"></a><span data-ttu-id="6fffa-104">平台</span><span class="sxs-lookup"><span data-stu-id="6fffa-104">Platforms</span></span>

<span data-ttu-id="6fffa-105">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fffa-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="6fffa-106">Description</span><span class="sxs-lookup"><span data-stu-id="6fffa-106">Description</span></span>

<span data-ttu-id="6fffa-107">在 Windows Server 2012 中， \_ (擴充 SRB 的儲存體要求 \_ 區塊) 會取代 \_ \_ 核心儲存體堆疊中 (舊版 SRB) 的 SCSI 要求區塊。</span><span class="sxs-lookup"><span data-stu-id="6fffa-107">In Windows Server 2012, a new structure, the STORAGE\_REQUEST\_BLOCK (extended SRB) replaces the SCSI\_REQUEST\_BLOCK (legacy SRB) in the core storage stack.</span></span> <span data-ttu-id="6fffa-108">擴充 SRBs 會複寫舊版 SRBs 的功能，但也可延伸和擴充。</span><span class="sxs-lookup"><span data-stu-id="6fffa-108">Extended SRBs replicate the functionality of the legacy SRBs, but are also extensible and scalable.</span></span>

<span data-ttu-id="6fffa-109">多重路徑 i/o (MPIO) 支援擴充 SRBs，並可讓裝置特定模組 (DSMs) 也可指定外延 SRB 支援。</span><span class="sxs-lookup"><span data-stu-id="6fffa-109">Multipath I/O (MPIO) supports extended SRBs and allows Device Specific Modules (DSMs) to specify extended SRB support as well.</span></span> <span data-ttu-id="6fffa-110">不過，為了讓多重路徑裝置的儲存體堆疊使用擴充 SRBs， **堆疊中的所有元件都必須支援延伸 SRBs，包括 DSM**。</span><span class="sxs-lookup"><span data-stu-id="6fffa-110">However, in order for a multipath device’s storage stack to use extended SRBs, **all components in the stack must support extended SRBs, including the DSM**.</span></span> <span data-ttu-id="6fffa-111">請注意，Microsoft 內建 DSM （即 MSDSM）支援擴充 SRBs。</span><span class="sxs-lookup"><span data-stu-id="6fffa-111">Note that the Microsoft in-box DSM, MSDSM, does support extended SRBs.</span></span>

<span data-ttu-id="6fffa-112">SCSI 通過 \_ \_ \_ EX 結構並不是延伸的 MPIO 傳遞結構的一部分，因為擴充的 scsi pass 可以是變數大小，視命令列偵錯工具 (CDB) 而定。</span><span class="sxs-lookup"><span data-stu-id="6fffa-112">The SCSI\_PASS\_THROUGH\_EX structure is not part of the extended MPIO pass through structure since the extended SCSI pass through can be of a variable size, depending on the command line debugger (CDB).</span></span> <span data-ttu-id="6fffa-113">相反地，擴充 MPIO 傳遞會有一個欄位，其描述從擴充 MPIO 通過結構開始到 SCSI 通過 \_ \_ \_ EX 結構的位移。</span><span class="sxs-lookup"><span data-stu-id="6fffa-113">Instead, the extended MPIO pass through has a field that describes the offset from the beginning of the extended MPIO pass through structure to the SCSI\_PASS\_THROUGH\_EX structure.</span></span> <span data-ttu-id="6fffa-114">呼叫端必須確認它們配置了適當大小的緩衝區，並正確地設定 SCSI 通過。</span><span class="sxs-lookup"><span data-stu-id="6fffa-114">The caller must make sure they allocate a buffer of the appropriate size and set the SCSI pass through offset correctly.</span></span> <span data-ttu-id="6fffa-115">只要呼叫端遵循擴充 SCSI 傳遞解說的規則，則應該不會有任何額外的工作可供他們使用擴充的 MPIO 傳遞。</span><span class="sxs-lookup"><span data-stu-id="6fffa-115">As long as the caller follows the rules for extended SCSI pass-throughs, then there should not be any extra work for them to use the extended MPIO pass through.</span></span>

> [!Note]  
> <span data-ttu-id="6fffa-116">如果 DSM 不支援擴充 SRBs，MPIO 將會透過具有 MPIO \_ IOCTL 旗標與 \_ \_ \_ DSM 旗標設定的要求，使擴充 mpio 傳遞失敗。</span><span class="sxs-lookup"><span data-stu-id="6fffa-116">If the DSM does not support extended SRBs, MPIO will fail extended MPIO pass through requests that have the MPIO\_IOCTL\_FLAG\_INVOLVE\_DSM flag set.</span></span>

 

## <a name="manifestation"></a><span data-ttu-id="6fffa-117">表現</span><span class="sxs-lookup"><span data-stu-id="6fffa-117">Manifestation</span></span>

<span data-ttu-id="6fffa-118">如果裝置的儲存體堆疊有任何部分（包括 DSM）不支援擴充 SRBs，則儲存體堆疊會還原為使用舊版 SRBs。</span><span class="sxs-lookup"><span data-stu-id="6fffa-118">If any part of the device’s storage stack, including DSM, does not support extended SRBs, the storage stack will revert to using legacy SRBs.</span></span>

## <a name="solution"></a><span data-ttu-id="6fffa-119">解決方法</span><span class="sxs-lookup"><span data-stu-id="6fffa-119">Solution</span></span>

<span data-ttu-id="6fffa-120">DSM 只有兩個 MPIO 需求可支援儲存體 \_ 要求 \_ 區塊：</span><span class="sxs-lookup"><span data-stu-id="6fffa-120">There are only two MPIO requirements for a DSM to support STORAGE\_REQUEST\_BLOCKS:</span></span>

-   <span data-ttu-id="6fffa-121">DSM 必須將其類型報告為 DsmType6</span><span class="sxs-lookup"><span data-stu-id="6fffa-121">The DSM must report its type as DsmType6</span></span>
-   <span data-ttu-id="6fffa-122">DSM 必須提供支援的 DSM \_ 位址 \_ 類型 \_ 函數</span><span class="sxs-lookup"><span data-stu-id="6fffa-122">The DSM must provide the DSM\_ADDRESS\_TYPE\_SUPPORTED function</span></span>

<span data-ttu-id="6fffa-123">如果 DSM 未回報 DsmType6 或回報 DsmType6，但未提供 DSM \_ 網址類別型支援的函式 \_ ，則 \_ MPIO 會假設 DSM 不支援外延 SRBs。</span><span class="sxs-lookup"><span data-stu-id="6fffa-123">If the DSM does not report DsmType6 or if it reports DsmType6 but does not provide the DSM\_ADDRESS\_TYPE\_SUPPORTED function, MPIO will assume the DSM does not support extended SRBs.</span></span>

<span data-ttu-id="6fffa-124">DSM \_ 位址 \_ 類型支援的 \_ 函數接受兩個參數，其中一個是網址類別型。</span><span class="sxs-lookup"><span data-stu-id="6fffa-124">The DSM\_ADDRESS\_TYPE\_SUPPORTED function accepts two parameters, one of which is an address type.</span></span> <span data-ttu-id="6fffa-125">此網址類別型必須是 srb 中所定義的其中一個儲存體 \_ 位址 \_ 類型 \_ \* 值。</span><span class="sxs-lookup"><span data-stu-id="6fffa-125">This address type must be one of the STORAGE\_ADDRESS\_TYPE\_\* values defined in srb.h.</span></span> <span data-ttu-id="6fffa-126">如果 DSM 支援指定的網址類別型，則必須傳回 TRUE，否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="6fffa-126">The DSM must return TRUE if it supports the given address type and FALSE if it does not.</span></span> <span data-ttu-id="6fffa-127">"Support" 的定義最終會由 DSM 組成。</span><span class="sxs-lookup"><span data-stu-id="6fffa-127">The definition of “support” is ultimately up to the DSM.</span></span> <span data-ttu-id="6fffa-128">MPIO 會使用此函式，以確保當 DSM 以 \_ 指定類型的 STOR 位址結構來取得延伸 SRB 時，將不會行為失常。</span><span class="sxs-lookup"><span data-stu-id="6fffa-128">MPIO uses this function to ensure that the DSM will not misbehave if it is handed an extended SRB with a STOR\_ADDRESS structure of the given type.</span></span> <span data-ttu-id="6fffa-129">因此，當列舉多重路徑裝置時，MPIO 通常會呼叫此函式，但是可以隨時呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="6fffa-129">As such, MPIO generally calls this function when a multipath device is being enumerated, but the function could be called at any time.</span></span>

<span data-ttu-id="6fffa-130">如果 DSM 從未觸及擴充 SRB 的 STOR \_ 位址，則可以針對任何有效的儲存體 \_ 網址類別型值傳回 TRUE \_ \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="6fffa-130">If a DSM never touches an extended SRB’s STOR\_ADDRESS, then it can return TRUE for any valid STORAGE\_ADDRESS\_TYPE\_\* value.</span></span> <span data-ttu-id="6fffa-131">請參閱 WDK 中的範例 DSM。</span><span class="sxs-lookup"><span data-stu-id="6fffa-131">Review the sample DSM in the WDK.</span></span>

<span data-ttu-id="6fffa-132">**其他重要注意事項**</span><span class="sxs-lookup"><span data-stu-id="6fffa-132">**Other important notes**</span></span>

-   <span data-ttu-id="6fffa-133">支援延伸 SRBs 的 DSMs 必須能夠處理 SCSI \_ 要求 \_ 區塊結構和儲存體 \_ 要求 \_ 區塊結構。</span><span class="sxs-lookup"><span data-stu-id="6fffa-133">DSMs that support extended SRBs must be able to handle both SCSI\_REQUEST\_BLOCK structures and STORAGE\_REQUEST\_BLOCK structures.</span></span> <span data-ttu-id="6fffa-134">由於 DSM 報告支援擴充 SRBs，並不表示它只會收到延伸的 SRBs。</span><span class="sxs-lookup"><span data-stu-id="6fffa-134">Just because a DSM reports that it supports extended SRBs does not mean that it will exclusively receive extended SRBs.</span></span> <span data-ttu-id="6fffa-135">除了擴充 SRBs，它可能仍會收到任何數目的舊版 SRBs，因此必須能夠同時處理這兩者。</span><span class="sxs-lookup"><span data-stu-id="6fffa-135">It may still receive any number of legacy SRBs in addition to extended SRBs, and therefore must be able to handle both.</span></span>
-   <span data-ttu-id="6fffa-136">我們在名為 srbhelper 的 WDK 中提供標頭檔，其中包含內嵌函式，可協助必須處理擴充和舊版 SRBs 的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6fffa-136">We have provided a header file in the WDK called srbhelper.h that contains inline functions to help drivers that must handle both extended and legacy SRBs.</span></span> <span data-ttu-id="6fffa-137">我們的範例 DSM 會使用此標頭，讓您可以使用它作為如何使用這些函式的範例。</span><span class="sxs-lookup"><span data-stu-id="6fffa-137">Our sample DSM uses this header so you can use it as an example of how to use these functions.</span></span>
-   <span data-ttu-id="6fffa-138">不支援擴充 SRBs 的 DSM 永遠不需要處理延伸的 SRBs。</span><span class="sxs-lookup"><span data-stu-id="6fffa-138">A DSM that does not support extended SRBs will never have to handle extended SRBs.</span></span>
-   <span data-ttu-id="6fffa-139">當 DSM 不支援指定的儲存體位址 (類型時，MPIO 可能會導致儲存體堆疊回復舊版 SRBs， \_ \_ \_ \* 否則支援擴充的 SRBs) 。</span><span class="sxs-lookup"><span data-stu-id="6fffa-139">It’s possible that a MPIO will cause the storage stack to fall back on legacy SRBs in the event that the DSM does not support a given STORAGE\_ADDRESS\_TYPE\_\* (but otherwise supports extended SRBs).</span></span>
-   <span data-ttu-id="6fffa-140">"BTL8" 是 \_ \_ \_ \* 目前為 Windows Server 2012 定義的唯一儲存體網址類別型。</span><span class="sxs-lookup"><span data-stu-id="6fffa-140">“BTL8” is the only STORAGE\_ADDRESS\_TYPE\_\*currently defined for Windows Server 2012.</span></span>

 

 




