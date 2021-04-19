---
title: ID3D12CommandQueueDownlevel：:P 重發方法
description: 將內容從 Direct3D 12 Texture2D 資源複製到視窗。 |ID3D12CommandQueueDownlevel：:P 重發方法
keywords:
- 現在時方法
- 目前的方法，ID3D12CommandQueueDownlevel 介面
- ID3D12CommandQueueDownlevel 介面，存在方法
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106995902"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="5804b-107">ID3D12CommandQueueDownlevel：:P 重發方法</span><span class="sxs-lookup"><span data-stu-id="5804b-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="5804b-108">將內容從 Direct3D 12 Texture2D 資源複製到視窗。</span><span class="sxs-lookup"><span data-stu-id="5804b-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="5804b-109">語法</span><span class="sxs-lookup"><span data-stu-id="5804b-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="5804b-110">參數</span><span class="sxs-lookup"><span data-stu-id="5804b-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="5804b-111">類型： **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="5804b-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="5804b-112">開啟的命令清單，Direct3D 12 會將目前的命令，然後為您關閉並提交。</span><span class="sxs-lookup"><span data-stu-id="5804b-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="5804b-113">類型： **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="5804b-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="5804b-114">包含要顯示之所需內容的資源，包含維度 [**D3D12 \_ 資源 \_ 維度 \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)，以及下列其中一種格式。</span><span class="sxs-lookup"><span data-stu-id="5804b-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="5804b-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="5804b-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="5804b-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="5804b-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="5804b-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="5804b-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="5804b-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="5804b-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="5804b-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="5804b-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="5804b-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="5804b-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="5804b-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="5804b-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="5804b-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="5804b-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="5804b-123">類型： **[HWND](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5804b-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5804b-124">應顯示內容的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="5804b-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="5804b-125">類型： **[D3D12 \_ 下層 \_ 目前的 \_ 旗標](d3d12_downlevel_present_flags.md)**</span><span class="sxs-lookup"><span data-stu-id="5804b-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="5804b-126">用以修改 **目前** 作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="5804b-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="5804b-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="5804b-127">Return value</span></span>

<span data-ttu-id="5804b-128">會在成功時傳回 **S_OK** ，否則會傳回失敗的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="5804b-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="5804b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5804b-129">Requirements</span></span>

| <span data-ttu-id="5804b-130">需求</span><span class="sxs-lookup"><span data-stu-id="5804b-130">Requirement</span></span> | <span data-ttu-id="5804b-131">值</span><span class="sxs-lookup"><span data-stu-id="5804b-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="5804b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5804b-132">Header</span></span> | <span data-ttu-id="5804b-133">d3d12downlevel。h</span><span class="sxs-lookup"><span data-stu-id="5804b-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="5804b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5804b-134">DLL</span></span>    | <span data-ttu-id="5804b-135">D3D12.dll 只 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="5804b-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5804b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5804b-136">See also</span></span>
* [<span data-ttu-id="5804b-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="5804b-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="5804b-138">Windows 7 上的 Direct3D 12 介面</span><span class="sxs-lookup"><span data-stu-id="5804b-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="5804b-139">Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) </span><span class="sxs-lookup"><span data-stu-id="5804b-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="5804b-140">Windows 7 上的 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5804b-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
