---
description: 建立異步資源載入器。
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: 'D3DX10CreateAsyncResourceLoader 函式 (D3DX10Async) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0539817ffff75c28af41289fc5197f6440a915bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993868"
---
# <a name="d3dx10createasyncresourceloader-function"></a><span data-ttu-id="61281-103">D3DX10CreateAsyncResourceLoader 函式</span><span class="sxs-lookup"><span data-stu-id="61281-103">D3DX10CreateAsyncResourceLoader function</span></span>

<span data-ttu-id="61281-104">建立異步資源載入器。</span><span class="sxs-lookup"><span data-stu-id="61281-104">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="61281-105">語法</span><span class="sxs-lookup"><span data-stu-id="61281-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="61281-106">參數</span><span class="sxs-lookup"><span data-stu-id="61281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61281-107">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61281-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61281-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61281-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="61281-109">資源模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="61281-109">Handle to the resource module.</span></span> <span data-ttu-id="61281-110">使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 來取得控制碼。</span><span class="sxs-lookup"><span data-stu-id="61281-110">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="61281-111">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61281-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61281-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61281-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="61281-113">HSrcModule 中資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="61281-113">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="61281-114">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="61281-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="61281-115">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="61281-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="61281-116">*ppDataLoader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61281-116">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61281-117">類型： **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="61281-117">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="61281-118">非同步資料處理器指標的位址 (參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="61281-118">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61281-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="61281-119">Return value</span></span>

<span data-ttu-id="61281-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61281-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61281-121">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="61281-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61281-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="61281-122">Requirements</span></span>



| <span data-ttu-id="61281-123">需求</span><span class="sxs-lookup"><span data-stu-id="61281-123">Requirement</span></span> | <span data-ttu-id="61281-124">值</span><span class="sxs-lookup"><span data-stu-id="61281-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61281-125">標頭</span><span class="sxs-lookup"><span data-stu-id="61281-125">Header</span></span><br/> | <dl> <span data-ttu-id="61281-126"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="61281-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61281-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61281-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61281-128">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="61281-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
