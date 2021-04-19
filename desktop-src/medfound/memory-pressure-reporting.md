---
description: 記憶體壓力報告可讓 Direct3D 應用程式判斷其影片記憶體工作集是否成長過大。
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: 記憶體壓力報告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996651"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="92fa0-103">記憶體壓力報告</span><span class="sxs-lookup"><span data-stu-id="92fa0-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="92fa0-104">記憶體壓力報告可讓 Direct3D 應用程式判斷其影片記憶體工作集是否成長過大。</span><span class="sxs-lookup"><span data-stu-id="92fa0-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="92fa0-105">*記憶體壓力* 是應用程式放在記憶體子系統上的需求。</span><span class="sxs-lookup"><span data-stu-id="92fa0-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="92fa0-106">雖然任何 Direct3D 應用程式都可以使用記憶體壓力報告，但這項功能特別適用于使用 Direct3D 呈現影片的應用程式。</span><span class="sxs-lookup"><span data-stu-id="92fa0-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="92fa0-107">影片播放通常受益于大量的緩衝，因此可以事先解碼框架。</span><span class="sxs-lookup"><span data-stu-id="92fa0-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="92fa0-108">雖然緩衝處理通常會使播放更順暢，但如果工作集成長太大，則可能會因為下列因素而導致效能降低：</span><span class="sxs-lookup"><span data-stu-id="92fa0-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="92fa0-109">記憶體可能會從快取中收回。</span><span class="sxs-lookup"><span data-stu-id="92fa0-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="92fa0-110">在最糟的情況下，這可能會發生在每個影片畫面上。</span><span class="sxs-lookup"><span data-stu-id="92fa0-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="92fa0-111">記憶體配置可能會放置在非最佳的記憶體區段中。</span><span class="sxs-lookup"><span data-stu-id="92fa0-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="92fa0-112">從 Windows 7 開始，Direct3D 可以報告關於影片記憶體壓力的一些統計資料：</span><span class="sxs-lookup"><span data-stu-id="92fa0-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="92fa0-113">進程在一段時間內收回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="92fa0-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="92fa0-114">放在非最非最佳記憶體區段中的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="92fa0-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="92fa0-115">粗略指出記憶體配置放在非最佳記憶體的整體效率。</span><span class="sxs-lookup"><span data-stu-id="92fa0-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="92fa0-116">此資訊可協助應用程式維護合理的工作集。</span><span class="sxs-lookup"><span data-stu-id="92fa0-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="92fa0-117">使用記憶體壓力報告</span><span class="sxs-lookup"><span data-stu-id="92fa0-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="92fa0-118">記憶體壓力報告使用現有的 **IDirect3DQuery9** 介面來查詢裝置。</span><span class="sxs-lookup"><span data-stu-id="92fa0-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="92fa0-119">已將新的查詢類型加入至 **D3DQUERYTYPE** 列舉。</span><span class="sxs-lookup"><span data-stu-id="92fa0-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="92fa0-120">若要使用此查詢，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="92fa0-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="92fa0-121">使用 **D3DQUERYTYPE \_ MEMORYPRESSURE** 旗標呼叫 **IDirect3DDevice9Ex：： CreateQuery** 。</span><span class="sxs-lookup"><span data-stu-id="92fa0-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="92fa0-122">這個方法會傳回 **IDirect3DQuery9** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="92fa0-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="92fa0-123">使用 **D3DISSUE \_ 開始** 旗標呼叫 **IDirect3DQuery9：： Issue** 開始度量間隔。</span><span class="sxs-lookup"><span data-stu-id="92fa0-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="92fa0-124">使用 **D3DISSUE \_ 結束** 旗標呼叫 **IDirect3DQuery9：： Issue** 。</span><span class="sxs-lookup"><span data-stu-id="92fa0-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="92fa0-125">呼叫 **IDirect3DQuery9：：** 以取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="92fa0-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="92fa0-126">此查詢會傳回 [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="92fa0-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="92fa0-127">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="92fa0-127">Example Code</span></span>

<span data-ttu-id="92fa0-128">下列範例顯示兩個測量記憶體壓力的函數。</span><span class="sxs-lookup"><span data-stu-id="92fa0-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="92fa0-129">第一個會開始測量間隔，而第二個則會抓取測量結果。</span><span class="sxs-lookup"><span data-stu-id="92fa0-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="92fa0-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="92fa0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92fa0-131">Direct3D 影片 Api</span><span class="sxs-lookup"><span data-stu-id="92fa0-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



