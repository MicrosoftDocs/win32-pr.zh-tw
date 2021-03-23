---
title: 設定和填入描述元堆積
description: 可以在命令清單上設定的描述項堆積型別，也就是包含描述項資料表的描述項，其中每一次最多隻能使用 (的描述中繼資料表) 。
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548381"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="ab570-103">設定和填入描述元堆積</span><span class="sxs-lookup"><span data-stu-id="ab570-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="ab570-104">可以在命令清單上設定的描述項堆積型別，也就是包含描述項資料表的描述項，其中每一次最多隻能使用 (的描述中繼資料表) 。</span><span class="sxs-lookup"><span data-stu-id="ab570-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="ab570-105">設定描述元堆積</span><span class="sxs-lookup"><span data-stu-id="ab570-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="ab570-106">填入描述元堆積</span><span class="sxs-lookup"><span data-stu-id="ab570-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="ab570-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab570-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="ab570-108">設定描述元堆積</span><span class="sxs-lookup"><span data-stu-id="ab570-108">Setting descriptor heaps</span></span>

<span data-ttu-id="ab570-109">可以在命令清單上設定的描述元堆積類型為：</span><span class="sxs-lookup"><span data-stu-id="ab570-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="ab570-110">命令清單上所設定的堆積也必須已建立為著色器可見。</span><span class="sxs-lookup"><span data-stu-id="ab570-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="ab570-111">有三種類型的命令清單： DIRECT、配套和計算。</span><span class="sxs-lookup"><span data-stu-id="ab570-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="ab570-112">在命令清單上設定描述項堆積之後，定義描述中繼資料表的後續呼叫會參考目前的描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="ab570-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="ab570-113">在命令清單的開頭，以及在命令清單上變更描述項堆積之後，會定義描述項資料表狀態。</span><span class="sxs-lookup"><span data-stu-id="ab570-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="ab570-114">重複設定相同的描述元堆積不會造成描述項資料表設定未定義。</span><span class="sxs-lookup"><span data-stu-id="ab570-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="ab570-115">相較之下，相較之下，只有在 (重複的呼叫設定相同堆積兩次不會產生錯誤) ;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="ab570-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="ab570-116">當任何命令清單呼叫組合時，所設定的描述元堆積必須符合狀態;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="ab570-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="ab570-117">這可讓配套來繼承和編輯命令清單的描述項資料表設定。</span><span class="sxs-lookup"><span data-stu-id="ab570-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="ab570-118">不會變更描述項資料表的配套 (只會繼承它們) 完全不需要設定描述元堆積，而只會繼承自呼叫命令清單。</span><span class="sxs-lookup"><span data-stu-id="ab570-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="ab570-119">當 (使用 [**ID3D12GraphicsCommandList：： SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)) 設定描述元堆積時，所使用的所有堆積都會設定在單一呼叫中 (而且所有先前設定的堆積都會由呼叫) 取消設定。</span><span class="sxs-lookup"><span data-stu-id="ab570-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="ab570-120">在此呼叫中，最多可以設定上面所列之每個類型的一個堆積。</span><span class="sxs-lookup"><span data-stu-id="ab570-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="ab570-121">填入描述元堆積</span><span class="sxs-lookup"><span data-stu-id="ab570-121">Populating descriptor heaps</span></span>

<span data-ttu-id="ab570-122">在應用程式建立描述元堆積之後，接著就可以在裝置上使用方法，將描述項直接產生到堆積，或從一個位置將描述項複製到另一個位置。</span><span class="sxs-lookup"><span data-stu-id="ab570-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="ab570-123">描述元堆積記憶體的初始內容尚未定義，因此，要求 GPU 或驅動程式參考未初始化的記憶體來進行轉譯，可能會導致未定義的結果，例如裝置重設。</span><span class="sxs-lookup"><span data-stu-id="ab570-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="ab570-124">如果應用程式將描述項堆積設定為可供 CPU 使用，則 CPU 可以呼叫方法來建立堆積中的描述元，並從就地複製以放置 (包括以立即、自由執行緒方式) 的堆積。</span><span class="sxs-lookup"><span data-stu-id="ab570-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="ab570-125">如果堆積已設定為 SHADER_VISIBLE，則不允許讀取 CPU。</span><span class="sxs-lookup"><span data-stu-id="ab570-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="ab570-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab570-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab570-127">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="ab570-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




