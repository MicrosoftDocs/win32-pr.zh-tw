---
title: 'D3DX11CreateAsyncResourceLoader 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立異步資源載入器。
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- D3DX11CreateAsyncResourceLoader 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035396"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="68c1f-106">D3DX11CreateAsyncResourceLoader 函式</span><span class="sxs-lookup"><span data-stu-id="68c1f-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="68c1f-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="68c1f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="68c1f-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="68c1f-108">See Remarks.</span></span>

 

<span data-ttu-id="68c1f-109">建立異步資源載入器。</span><span class="sxs-lookup"><span data-stu-id="68c1f-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c1f-110">語法</span><span class="sxs-lookup"><span data-stu-id="68c1f-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="68c1f-111">參數</span><span class="sxs-lookup"><span data-stu-id="68c1f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c1f-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68c1f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68c1f-113">類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68c1f-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="68c1f-114">資源模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="68c1f-114">Handle to the resource module.</span></span> <span data-ttu-id="68c1f-115">使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 來取得控制碼。</span><span class="sxs-lookup"><span data-stu-id="68c1f-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="68c1f-116">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68c1f-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68c1f-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68c1f-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="68c1f-118">HSrcModule 中資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="68c1f-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="68c1f-119">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="68c1f-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="68c1f-120">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="68c1f-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="68c1f-121">*ppDataLoader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68c1f-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68c1f-122">類型： **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="68c1f-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="68c1f-123">非同步資料載入器指標的位址 (參閱 [**ID3DX11DataLoader 介面**](id3dx11dataloader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="68c1f-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c1f-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="68c1f-124">Return value</span></span>

<span data-ttu-id="68c1f-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68c1f-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68c1f-126">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="68c1f-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68c1f-127">備註</span><span class="sxs-lookup"><span data-stu-id="68c1f-127">Remarks</span></span>

<span data-ttu-id="68c1f-128">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="68c1f-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="68c1f-129">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="68c1f-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="68c1f-130">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="68c1f-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c1f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="68c1f-131">Requirements</span></span>



| <span data-ttu-id="68c1f-132">需求</span><span class="sxs-lookup"><span data-stu-id="68c1f-132">Requirement</span></span> | <span data-ttu-id="68c1f-133">值</span><span class="sxs-lookup"><span data-stu-id="68c1f-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c1f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="68c1f-134">Header</span></span><br/>  | <dl> <span data-ttu-id="68c1f-135"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="68c1f-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="68c1f-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="68c1f-136">Library</span></span><br/> | <dl> <span data-ttu-id="68c1f-137"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68c1f-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="68c1f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68c1f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c1f-139">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="68c1f-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

