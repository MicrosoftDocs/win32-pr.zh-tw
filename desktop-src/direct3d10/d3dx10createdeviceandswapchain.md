---
description: 建立最佳的 Direct3D 裝置和交換鏈。
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: 'D3DX10CreateDeviceAndSwapChain 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323196"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="dff28-103">D3DX10CreateDeviceAndSwapChain 函式</span><span class="sxs-lookup"><span data-stu-id="dff28-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="dff28-104">建立最佳的 Direct3D 裝置和交換鏈。</span><span class="sxs-lookup"><span data-stu-id="dff28-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="dff28-105">語法</span><span class="sxs-lookup"><span data-stu-id="dff28-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="dff28-106">參數</span><span class="sxs-lookup"><span data-stu-id="dff28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff28-107">*pAdapter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff28-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-108">類型： **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="dff28-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="dff28-109">[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)的指標。</span><span class="sxs-lookup"><span data-stu-id="dff28-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="dff28-110">*DriverType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff28-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-111">類型： **[ **D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="dff28-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="dff28-112">裝置的驅動程式類型。</span><span class="sxs-lookup"><span data-stu-id="dff28-112">The type of driver for the device.</span></span> <span data-ttu-id="dff28-113">請參閱 [**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)。</span><span class="sxs-lookup"><span data-stu-id="dff28-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="dff28-114">*軟體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff28-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-115">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dff28-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dff28-116">執行軟體轉譯器之 DLL 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dff28-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="dff28-117">如果 DriverType 為非軟體，則必須是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dff28-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="dff28-118">您可以使用 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)、 [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)或 [GETMODULEHANDLE](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 DLL 的 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="dff28-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="dff28-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="dff28-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dff28-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dff28-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="dff28-121">Optional.</span></span> <span data-ttu-id="dff28-122">裝置建立旗標 (查看啟用 [API 層](d3d10-graphics-programming-guide-api-features-layers.md)的 [**D3D10 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)標) 。</span><span class="sxs-lookup"><span data-stu-id="dff28-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="dff28-123">這些旗標可以是位 OR。</span><span class="sxs-lookup"><span data-stu-id="dff28-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="dff28-124">*pSwapChainDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff28-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-125">類型： **[ **DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="dff28-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="dff28-126">交換鏈的描述。</span><span class="sxs-lookup"><span data-stu-id="dff28-126">Description of the swap chain.</span></span> <span data-ttu-id="dff28-127">請參閱 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)。</span><span class="sxs-lookup"><span data-stu-id="dff28-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="dff28-128">*ppSwapChain* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dff28-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-129">類型： **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="dff28-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="dff28-130">[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)指標的位址。</span><span class="sxs-lookup"><span data-stu-id="dff28-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="dff28-131">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dff28-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dff28-132">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="dff28-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="dff28-133">[**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)的指標位址，此介面會接收新建立的裝置。</span><span class="sxs-lookup"><span data-stu-id="dff28-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff28-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="dff28-134">Return value</span></span>

<span data-ttu-id="dff28-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dff28-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dff28-136">這個方法會傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="dff28-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dff28-137">備註</span><span class="sxs-lookup"><span data-stu-id="dff28-137">Remarks</span></span>

<span data-ttu-id="dff28-138">若要建立最佳裝置，這個方法會執行一個以上的裝置建立選項。</span><span class="sxs-lookup"><span data-stu-id="dff28-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="dff28-139">首先，此方法會嘗試建立10.1 裝置 (和交換鏈) 。</span><span class="sxs-lookup"><span data-stu-id="dff28-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="dff28-140">如果失敗，方法會嘗試建立10.0 裝置。</span><span class="sxs-lookup"><span data-stu-id="dff28-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="dff28-141">如果失敗，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="dff28-141">If that fails, the method will fail.</span></span> <span data-ttu-id="dff28-142">如果您的應用程式只需要建立10.1 裝置或僅限10.0 裝置，請改用這些 Api：</span><span class="sxs-lookup"><span data-stu-id="dff28-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="dff28-143">使用 [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) 建立僅) 裝置和交換鏈的 Direct3D 10.0 (。</span><span class="sxs-lookup"><span data-stu-id="dff28-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="dff28-144">使用 [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) 建立僅) 裝置和交換鏈的 Direct3D 10.1 (。</span><span class="sxs-lookup"><span data-stu-id="dff28-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="dff28-145">此方法需要 Windows Vista Service Pack 1。</span><span class="sxs-lookup"><span data-stu-id="dff28-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff28-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="dff28-146">Requirements</span></span>



| <span data-ttu-id="dff28-147">需求</span><span class="sxs-lookup"><span data-stu-id="dff28-147">Requirement</span></span> | <span data-ttu-id="dff28-148">值</span><span class="sxs-lookup"><span data-stu-id="dff28-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dff28-149">標頭</span><span class="sxs-lookup"><span data-stu-id="dff28-149">Header</span></span><br/> | <dl> <span data-ttu-id="dff28-150"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="dff28-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff28-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dff28-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff28-152">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="dff28-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
