---
title: 'D3DX11CreateThreadPump 函式 (D3DX11core) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立執行緒抽取。
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- D3DX11CreateThreadPump 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974601"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="25bbf-106">D3DX11CreateThreadPump 函式</span><span class="sxs-lookup"><span data-stu-id="25bbf-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="25bbf-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="25bbf-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="25bbf-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="25bbf-108">See Remarks.</span></span>

 

<span data-ttu-id="25bbf-109">建立執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="25bbf-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="25bbf-110">語法</span><span class="sxs-lookup"><span data-stu-id="25bbf-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="25bbf-111">參數</span><span class="sxs-lookup"><span data-stu-id="25bbf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25bbf-112">*cIoThreads* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25bbf-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25bbf-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25bbf-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25bbf-114">要建立的 i/o 執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="25bbf-114">The number of I/O threads to create.</span></span> <span data-ttu-id="25bbf-115">如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="25bbf-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="25bbf-116">*cProcThreads* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25bbf-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25bbf-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25bbf-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25bbf-118">要建立的進程執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="25bbf-118">The number of process threads to create.</span></span> <span data-ttu-id="25bbf-119">如果指定0，Direct3D 將會根據硬體設定嘗試計算最佳的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="25bbf-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="25bbf-120">*ppThreadPump* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="25bbf-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25bbf-121">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="25bbf-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="25bbf-122">建立的執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="25bbf-122">The created thread pump.</span></span> <span data-ttu-id="25bbf-123">請參閱 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="25bbf-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25bbf-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="25bbf-124">Return value</span></span>

<span data-ttu-id="25bbf-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25bbf-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25bbf-126">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="25bbf-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25bbf-127">備註</span><span class="sxs-lookup"><span data-stu-id="25bbf-127">Remarks</span></span>

<span data-ttu-id="25bbf-128">執行緒抽取是非常耗費資源的物件。</span><span class="sxs-lookup"><span data-stu-id="25bbf-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="25bbf-129">每個應用程式只應建立一個執行緒抽取。</span><span class="sxs-lookup"><span data-stu-id="25bbf-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="25bbf-130">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="25bbf-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="25bbf-131">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="25bbf-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="25bbf-132">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="25bbf-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="25bbf-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="25bbf-133">Requirements</span></span>



| <span data-ttu-id="25bbf-134">需求</span><span class="sxs-lookup"><span data-stu-id="25bbf-134">Requirement</span></span> | <span data-ttu-id="25bbf-135">值</span><span class="sxs-lookup"><span data-stu-id="25bbf-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25bbf-136">標頭</span><span class="sxs-lookup"><span data-stu-id="25bbf-136">Header</span></span><br/>  | <dl> <span data-ttu-id="25bbf-137"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="25bbf-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="25bbf-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="25bbf-138">Library</span></span><br/> | <dl> <span data-ttu-id="25bbf-139"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="25bbf-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25bbf-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25bbf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25bbf-141">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="25bbf-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

