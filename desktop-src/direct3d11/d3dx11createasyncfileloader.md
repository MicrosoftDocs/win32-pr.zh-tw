---
title: 'D3DX11CreateAsyncFileLoader 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立異步檔案載入器。
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- D3DX11CreateAsyncFileLoader 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637b2eddb035d937315582188295d93d9fd0e9b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992302"
---
# <a name="d3dx11createasyncfileloader-function"></a><span data-ttu-id="ae988-106">D3DX11CreateAsyncFileLoader 函式</span><span class="sxs-lookup"><span data-stu-id="ae988-106">D3DX11CreateAsyncFileLoader function</span></span>

> [!Note]  
> <span data-ttu-id="ae988-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ae988-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="ae988-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ae988-108">See Remarks.</span></span>

 

<span data-ttu-id="ae988-109">建立異步檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="ae988-109">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae988-110">語法</span><span class="sxs-lookup"><span data-stu-id="ae988-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="ae988-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae988-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae988-112">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae988-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae988-113">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ae988-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ae988-114">要載入的檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="ae988-114">The name of the file to load.</span></span> <span data-ttu-id="ae988-115">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="ae988-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ae988-116">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="ae988-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ae988-117">*ppDataLoader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae988-117">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae988-118">類型： **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae988-118">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="ae988-119">非同步資料載入器指標的位址 (參閱 [**ID3DX11DataLoader 介面**](id3dx11dataloader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ae988-119">Address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae988-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae988-120">Return value</span></span>

<span data-ttu-id="ae988-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae988-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae988-122">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ae988-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae988-123">備註</span><span class="sxs-lookup"><span data-stu-id="ae988-123">Remarks</span></span>

<span data-ttu-id="ae988-124">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="ae988-124">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="ae988-125">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="ae988-125">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="ae988-126">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="ae988-126">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae988-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae988-127">Requirements</span></span>



| <span data-ttu-id="ae988-128">需求</span><span class="sxs-lookup"><span data-stu-id="ae988-128">Requirement</span></span> | <span data-ttu-id="ae988-129">值</span><span class="sxs-lookup"><span data-stu-id="ae988-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae988-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ae988-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ae988-131"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae988-131"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="ae988-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="ae988-132">Library</span></span><br/> | <dl> <span data-ttu-id="ae988-133"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae988-133"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ae988-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae988-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae988-135">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="ae988-135">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

