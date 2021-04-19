---
title: ID3D12DeviceDownlevel：： QueryVideoMemoryInfo 方法
description: 將內容從 Direct3D 12 Texture2D 資源複製到視窗。 |ID3D12DeviceDownlevel：： QueryVideoMemoryInfo 方法
keywords:
- QueryVideoMemoryInfo 方法
- QueryVideoMemoryInfo 方法，ID3D12DeviceDownlevel 介面
- ID3D12DeviceDownlevel 介面，QueryVideoMemoryInfo 方法
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992335"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="0d537-107">ID3D12DeviceDownlevel：： QueryVideoMemoryInfo 方法</span><span class="sxs-lookup"><span data-stu-id="0d537-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="0d537-108">提供 Windows 7 的記憶體統計資料。</span><span class="sxs-lookup"><span data-stu-id="0d537-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="0d537-109">這個方法相當於 [IDXGIAdapter3：： QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo)，無法在 Windows 7 上使用。</span><span class="sxs-lookup"><span data-stu-id="0d537-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d537-110">語法</span><span class="sxs-lookup"><span data-stu-id="0d537-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="0d537-111">參數</span><span class="sxs-lookup"><span data-stu-id="0d537-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="0d537-112">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="0d537-112">Type: **UINT**</span></span>

<span data-ttu-id="0d537-113">指定要查詢其影片記憶體資訊的裝置實體介面卡。</span><span class="sxs-lookup"><span data-stu-id="0d537-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="0d537-114">若為單一 GPU 作業，請將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="0d537-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="0d537-115">如果有多個 GPU 節點，請將此設定為節點的索引， (裝置的實體介面卡) 來查詢影片的記憶體資訊。</span><span class="sxs-lookup"><span data-stu-id="0d537-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="0d537-116">請參閱 [多介面卡系統](multi-engine.md)。</span><span class="sxs-lookup"><span data-stu-id="0d537-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="0d537-117">類型： **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="0d537-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="0d537-118">指定將群組識別為本機或非本機的 **DXGI_MEMORY_SEGMENT_GROUP** 。</span><span class="sxs-lookup"><span data-stu-id="0d537-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="0d537-119">類型： **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="0d537-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="0d537-120">以目前的值填滿 **DXGI_QUERY_VIDEO_MEMORY_INFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="0d537-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d537-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d537-121">Return value</span></span>

<span data-ttu-id="0d537-122">會在成功時傳回 **S_OK** ，否則會傳回失敗的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="0d537-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d537-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d537-123">Requirements</span></span>

| <span data-ttu-id="0d537-124">需求</span><span class="sxs-lookup"><span data-stu-id="0d537-124">Requirement</span></span> | <span data-ttu-id="0d537-125">值</span><span class="sxs-lookup"><span data-stu-id="0d537-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="0d537-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0d537-126">Header</span></span> | <span data-ttu-id="0d537-127">d3d12downlevel .h 和 dxgi1_4。h</span><span class="sxs-lookup"><span data-stu-id="0d537-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="0d537-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0d537-128">DLL</span></span>    | <span data-ttu-id="0d537-129">D3D12.dll 只 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="0d537-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0d537-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d537-130">See also</span></span>
* [<span data-ttu-id="0d537-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="0d537-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="0d537-132">Windows 7 上的 Direct3D 12 介面</span><span class="sxs-lookup"><span data-stu-id="0d537-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="0d537-133">Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) </span><span class="sxs-lookup"><span data-stu-id="0d537-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="0d537-134">Windows 7 上的 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0d537-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
