---
description: 從未壓縮的 ID3DXPRTBuffer 物件建立壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區。 此函式應該搭配每個頂點或磁片區緩衝區使用。
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: 'D3DXCreatePRTCompBuffer 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322944"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="017b9-104">D3DXCreatePRTCompBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="017b9-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="017b9-105">從未壓縮的 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件建立壓縮的預先計算 radiance 傳輸 (PRT) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="017b9-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="017b9-106">此函式應該搭配每個頂點或磁片區緩衝區使用。</span><span class="sxs-lookup"><span data-stu-id="017b9-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="017b9-107">語法</span><span class="sxs-lookup"><span data-stu-id="017b9-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="017b9-108">參數</span><span class="sxs-lookup"><span data-stu-id="017b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="017b9-109">*品質* \[在\]</span><span class="sxs-lookup"><span data-stu-id="017b9-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-110">類型： **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="017b9-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="017b9-111">球形調和 (SH) 壓縮的品質。</span><span class="sxs-lookup"><span data-stu-id="017b9-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="017b9-112">請參閱 [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)。</span><span class="sxs-lookup"><span data-stu-id="017b9-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="017b9-113">*NumClusters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="017b9-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="017b9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="017b9-115">要用於壓縮的群集數目。</span><span class="sxs-lookup"><span data-stu-id="017b9-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="017b9-116">*NumPCA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="017b9-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="017b9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="017b9-118">每個叢集中要使用的主體元件分析數目 (PCA) 基礎向量。</span><span class="sxs-lookup"><span data-stu-id="017b9-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="017b9-119">*pCB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="017b9-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-120">類型： **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="017b9-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="017b9-121">[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)回呼函式的選擇性指標，可用來計算已完成的 PRT 壓縮計算百分比。</span><span class="sxs-lookup"><span data-stu-id="017b9-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="017b9-122">必須實回呼函式來傳回， \_ 才能繼續執行壓縮常式。</span><span class="sxs-lookup"><span data-stu-id="017b9-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="017b9-123">任何其他值都會中止壓縮。</span><span class="sxs-lookup"><span data-stu-id="017b9-123">Any other value will halt compression.</span></span> <span data-ttu-id="017b9-124">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="017b9-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="017b9-125">*lpUserCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="017b9-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-126">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="017b9-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="017b9-127">傳遞至 [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) 回呼函式的使用者定義值的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="017b9-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="017b9-128">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="017b9-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="017b9-129">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="017b9-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="017b9-130">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="017b9-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-131">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="017b9-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="017b9-132">將壓縮之未壓縮 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="017b9-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="017b9-133">*ppBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="017b9-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="017b9-134">類型： **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="017b9-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="017b9-135">輸出 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="017b9-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="017b9-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="017b9-136">Return value</span></span>

<span data-ttu-id="017b9-137">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="017b9-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="017b9-138">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="017b9-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="017b9-139">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="017b9-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="017b9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="017b9-140">Requirements</span></span>



| <span data-ttu-id="017b9-141">需求</span><span class="sxs-lookup"><span data-stu-id="017b9-141">Requirement</span></span> | <span data-ttu-id="017b9-142">值</span><span class="sxs-lookup"><span data-stu-id="017b9-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="017b9-143">標頭</span><span class="sxs-lookup"><span data-stu-id="017b9-143">Header</span></span><br/>  | <dl> <span data-ttu-id="017b9-144"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="017b9-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="017b9-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="017b9-145">Library</span></span><br/> | <dl> <span data-ttu-id="017b9-146"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="017b9-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="017b9-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="017b9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017b9-148">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="017b9-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="017b9-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="017b9-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="017b9-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="017b9-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
