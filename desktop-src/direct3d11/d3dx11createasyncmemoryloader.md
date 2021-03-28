---
title: 'D3DX11CreateAsyncMemoryLoader 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立異步記憶體載入器。
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- D3DX11CreateAsyncMemoryLoader 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992295"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="ab7d6-106">D3DX11CreateAsyncMemoryLoader 函式</span><span class="sxs-lookup"><span data-stu-id="ab7d6-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="ab7d6-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="ab7d6-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-108">See Remarks.</span></span>

 

<span data-ttu-id="ab7d6-109">建立異步記憶體載入器。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7d6-110">語法</span><span class="sxs-lookup"><span data-stu-id="ab7d6-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="ab7d6-111">參數</span><span class="sxs-lookup"><span data-stu-id="ab7d6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab7d6-112">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab7d6-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7d6-113">類型： **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab7d6-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab7d6-114">資料的指標。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="ab7d6-115">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab7d6-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7d6-116">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab7d6-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab7d6-117">資料的大小。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="ab7d6-118">*ppDataLoader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab7d6-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7d6-119">類型： **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab7d6-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="ab7d6-120">非同步資料載入器指標的位址 (參閱 [**ID3DX11DataLoader 介面**](id3dx11dataloader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab7d6-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab7d6-121">Return value</span></span>

<span data-ttu-id="ab7d6-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab7d6-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab7d6-123">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab7d6-124">備註</span><span class="sxs-lookup"><span data-stu-id="ab7d6-124">Remarks</span></span>

<span data-ttu-id="ab7d6-125">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="ab7d6-126">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="ab7d6-127">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="ab7d6-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7d6-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab7d6-128">Requirements</span></span>



| <span data-ttu-id="ab7d6-129">需求</span><span class="sxs-lookup"><span data-stu-id="ab7d6-129">Requirement</span></span> | <span data-ttu-id="ab7d6-130">值</span><span class="sxs-lookup"><span data-stu-id="ab7d6-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7d6-131">標頭</span><span class="sxs-lookup"><span data-stu-id="ab7d6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ab7d6-132"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7d6-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="ab7d6-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab7d6-133">Library</span></span><br/> | <dl> <span data-ttu-id="ab7d6-134"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab7d6-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ab7d6-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab7d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7d6-136">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="ab7d6-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

