---
description: 從 Direct3D 10.0 介面指標取得 Direct3D 10.1 裝置介面指標。
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: 'D3DX10GetFeatureLevel1 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991441"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="a0143-103">D3DX10GetFeatureLevel1 函式</span><span class="sxs-lookup"><span data-stu-id="a0143-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="a0143-104">從 Direct3D 10.0 介面指標取得 Direct3D 10.1 裝置介面指標。</span><span class="sxs-lookup"><span data-stu-id="a0143-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0143-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0143-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="a0143-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0143-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0143-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0143-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0143-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a0143-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a0143-109">Direct3D 10.0 裝置的指標 (查看 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) 介面) 。</span><span class="sxs-lookup"><span data-stu-id="a0143-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="a0143-110">*ppDevice* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a0143-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0143-111">類型： **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="a0143-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="a0143-112">Direct3D 10.1 裝置的指標 (查看 [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) 介面) 。</span><span class="sxs-lookup"><span data-stu-id="a0143-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0143-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0143-113">Return value</span></span>

<span data-ttu-id="a0143-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0143-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0143-115">此函數會傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="a0143-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="a0143-116">如果可以取得 Direct3D 10.1 裝置介面，此函式會成功，並使用 *ppDevice* 參數將指標傳遞至10.1 介面。</span><span class="sxs-lookup"><span data-stu-id="a0143-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="a0143-117">如果無法取得 Direct3D 10.1 裝置介面，此函式會傳回 E \_ 失敗，而且不會傳回任何 *ppDevice* 參數的任何參數。</span><span class="sxs-lookup"><span data-stu-id="a0143-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0143-118">備註</span><span class="sxs-lookup"><span data-stu-id="a0143-118">Remarks</span></span>

<span data-ttu-id="a0143-119">若要讓此函式成功，您必須使用 [**D3DX10CreateDevice**](d3dx10createdevice.md)函數、 [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)函式、 [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)函數或 [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)函數的呼叫來取得提供的 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)指標。</span><span class="sxs-lookup"><span data-stu-id="a0143-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="a0143-120">您只能在執行 Windows Vista Service Pack 1 或更新版本的電腦上，以及安裝 Direct3D 10.1 相容硬體的電腦上建立 Direct3D 10.1 裝置。</span><span class="sxs-lookup"><span data-stu-id="a0143-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="a0143-121">此函式會 \_ 在任何電腦上傳回 E 失敗，而不符合這些需求。</span><span class="sxs-lookup"><span data-stu-id="a0143-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="a0143-122">不過，您可以在已安裝 D3DX10 DLL 的任何 Windows 版本上呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="a0143-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0143-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0143-123">Requirements</span></span>



| <span data-ttu-id="a0143-124">需求</span><span class="sxs-lookup"><span data-stu-id="a0143-124">Requirement</span></span> | <span data-ttu-id="a0143-125">值</span><span class="sxs-lookup"><span data-stu-id="a0143-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0143-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a0143-126">Header</span></span><br/> | <dl> <span data-ttu-id="a0143-127"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0143-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0143-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0143-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0143-129">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="a0143-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




