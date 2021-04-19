---
description: 取得已載入記憶體之映射的相關資訊。
ms.assetid: 6750116a-ad4f-4102-aba9-6ef32c367be4
title: 'D3DX10GetImageInfoFromMemory 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 677ce6a2ac8e4e165ca0a2bbb64b6254870e4ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986518"
---
# <a name="d3dx10getimageinfofrommemory-function"></a><span data-ttu-id="bd34e-103">D3DX10GetImageInfoFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="bd34e-103">D3DX10GetImageInfoFromMemory function</span></span>

<span data-ttu-id="bd34e-104">取得已載入記憶體之映射的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd34e-104">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd34e-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd34e-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="bd34e-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd34e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd34e-107">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd34e-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd34e-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd34e-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd34e-109">記憶體中影像的指標。</span><span class="sxs-lookup"><span data-stu-id="bd34e-109">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="bd34e-110">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd34e-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd34e-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd34e-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd34e-112">記憶體中影像的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd34e-112">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bd34e-113">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd34e-113">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd34e-114">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd34e-114">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="bd34e-115">選擇性的執行緒抽取，可用來以非同步方式載入資訊。</span><span class="sxs-lookup"><span data-stu-id="bd34e-115">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="bd34e-116">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bd34e-116">Can be **NULL**.</span></span> <span data-ttu-id="bd34e-117">請參閱 [**ID3DX10ThreadPump**](id3dx10threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="bd34e-117">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd34e-118">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd34e-118">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd34e-119">類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd34e-119">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="bd34e-120">記憶體中影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd34e-120">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="bd34e-121">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bd34e-121">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd34e-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="bd34e-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="bd34e-123">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="bd34e-123">A pointer to the return value.</span></span> <span data-ttu-id="bd34e-124">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bd34e-124">May be **NULL**.</span></span> <span data-ttu-id="bd34e-125">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="bd34e-125">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd34e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd34e-126">Return value</span></span>

<span data-ttu-id="bd34e-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd34e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd34e-128">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bd34e-128">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd34e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd34e-129">Requirements</span></span>



| <span data-ttu-id="bd34e-130">需求</span><span class="sxs-lookup"><span data-stu-id="bd34e-130">Requirement</span></span> | <span data-ttu-id="bd34e-131">值</span><span class="sxs-lookup"><span data-stu-id="bd34e-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd34e-132">標頭</span><span class="sxs-lookup"><span data-stu-id="bd34e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="bd34e-133"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd34e-133"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="bd34e-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd34e-134">Library</span></span><br/> | <dl> <span data-ttu-id="bd34e-135"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd34e-135"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bd34e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd34e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd34e-137">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="bd34e-137">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
