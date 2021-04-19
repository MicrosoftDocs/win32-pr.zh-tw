---
description: 建立最佳的 Direct3D 10 裝置，以代表顯示配接器。 如果可以建立 Direct3D 10.1 相容裝置，就可以從傳回的裝置介面指標取得 ID3D10Device1 介面指標。
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: 'D3DX10CreateDevice 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976516"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="2eca1-104">D3DX10CreateDevice 函式</span><span class="sxs-lookup"><span data-stu-id="2eca1-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="2eca1-105">建立最佳的 Direct3D 10 裝置，以代表顯示配接器。</span><span class="sxs-lookup"><span data-stu-id="2eca1-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="2eca1-106">如果可以建立 Direct3D 10.1 相容裝置，就可以從傳回的裝置介面指標取得 [**ID3D10Device1 介面**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) 指標。</span><span class="sxs-lookup"><span data-stu-id="2eca1-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eca1-107">語法</span><span class="sxs-lookup"><span data-stu-id="2eca1-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="2eca1-108">參數</span><span class="sxs-lookup"><span data-stu-id="2eca1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eca1-109">*pAdapter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2eca1-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eca1-110">類型： **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="2eca1-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="2eca1-111">顯示配接器的指標 (在建立硬體裝置時看到 [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) 介面) ;否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2eca1-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="2eca1-112">如果在建立硬體裝置時指定了 **Null** ，Direct3D 將會使用 [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) 介面所列舉的第一個介面卡。</span><span class="sxs-lookup"><span data-stu-id="2eca1-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2eca1-113">*DriverType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2eca1-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eca1-114">類型： **[ **D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="2eca1-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="2eca1-115">裝置驅動程式類型 (查看 [**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) 列舉) 。</span><span class="sxs-lookup"><span data-stu-id="2eca1-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="2eca1-116">驅動程式類型可決定您將建立的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="2eca1-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="2eca1-117">*軟體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2eca1-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eca1-118">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eca1-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2eca1-119">已載入模組的控制碼，可執行軟體驅動程式 (例如 D3D10Ref.dll) 。</span><span class="sxs-lookup"><span data-stu-id="2eca1-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="2eca1-120">若要取得控制碼，請呼叫 [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函數。</span><span class="sxs-lookup"><span data-stu-id="2eca1-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="2eca1-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2eca1-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eca1-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eca1-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2eca1-123">裝置建立旗標 (查看啟用 [API 層](d3d10-graphics-programming-guide-api-features-layers.md)的 [**D3D10 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)標列舉) 。</span><span class="sxs-lookup"><span data-stu-id="2eca1-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="2eca1-124">這些旗標可以是位 OR。</span><span class="sxs-lookup"><span data-stu-id="2eca1-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="2eca1-125">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2eca1-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eca1-126">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="2eca1-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="2eca1-127">所建立之裝置的指標位址 (查看 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) 介面) 。</span><span class="sxs-lookup"><span data-stu-id="2eca1-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eca1-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="2eca1-128">Return value</span></span>

<span data-ttu-id="2eca1-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2eca1-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2eca1-130">此函數會傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="2eca1-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2eca1-131">備註</span><span class="sxs-lookup"><span data-stu-id="2eca1-131">Remarks</span></span>

<span data-ttu-id="2eca1-132">此函式會嘗試為硬體建立最佳裝置。</span><span class="sxs-lookup"><span data-stu-id="2eca1-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="2eca1-133">首先，此函式會嘗試建立10.1 裝置。</span><span class="sxs-lookup"><span data-stu-id="2eca1-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="2eca1-134">如果無法建立10.1 裝置，此函式會嘗試建立10.0 裝置。</span><span class="sxs-lookup"><span data-stu-id="2eca1-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="2eca1-135">如果未成功建立任何裝置，則函式會傳回 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="2eca1-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="2eca1-136">如果您的應用程式只需要建立10.1 裝置或僅限10.0 裝置，請改為使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="2eca1-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="2eca1-137">您只能使用 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) 函式來建立 Direct3D 10.0 裝置。</span><span class="sxs-lookup"><span data-stu-id="2eca1-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="2eca1-138">您只能使用 [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) 函式來建立 Direct3D 10.1 裝置。</span><span class="sxs-lookup"><span data-stu-id="2eca1-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="2eca1-139">您可以使用 [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md)函數，從 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)介面指標取得 [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)介面指標。</span><span class="sxs-lookup"><span data-stu-id="2eca1-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="2eca1-140">只能在執行 Windows Vista Service Pack 1 或更新版本的電腦上，以及安裝 Direct3D 10.1 相容硬體的電腦上建立 Direct3D 10.1 裝置。</span><span class="sxs-lookup"><span data-stu-id="2eca1-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="2eca1-141">不過，在執行任何已安裝 D3DX10 DLL 的 Windows 版本的電腦上呼叫此函式是合法的。</span><span class="sxs-lookup"><span data-stu-id="2eca1-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eca1-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eca1-142">Requirements</span></span>



| <span data-ttu-id="2eca1-143">需求</span><span class="sxs-lookup"><span data-stu-id="2eca1-143">Requirement</span></span> | <span data-ttu-id="2eca1-144">值</span><span class="sxs-lookup"><span data-stu-id="2eca1-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eca1-145">標頭</span><span class="sxs-lookup"><span data-stu-id="2eca1-145">Header</span></span><br/> | <dl> <span data-ttu-id="2eca1-146"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="2eca1-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eca1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2eca1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eca1-148">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="2eca1-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
