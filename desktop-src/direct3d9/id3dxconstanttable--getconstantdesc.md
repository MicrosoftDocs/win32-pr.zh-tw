---
description: 取得常數資料表中常數描述陣列的指標。
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable：： GetConstantDesc 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946120"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="4ec29-103">ID3DXConstantTable：： GetConstantDesc 方法</span><span class="sxs-lookup"><span data-stu-id="4ec29-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="4ec29-104">取得常數資料表中常數描述陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="4ec29-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec29-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ec29-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="4ec29-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ec29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec29-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ec29-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec29-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4ec29-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4ec29-109">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ec29-109">Unique identifier to a constant.</span></span> <span data-ttu-id="4ec29-110">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec29-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec29-111">*pDesc* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4ec29-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec29-112">類型： **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ec29-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="4ec29-113">傳回描述陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="4ec29-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="4ec29-114">請參閱 [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec29-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec29-115">*pCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4ec29-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec29-116">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ec29-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4ec29-117">提供的輸入必須是陣列的大小上限。</span><span class="sxs-lookup"><span data-stu-id="4ec29-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="4ec29-118">輸出是當函式傳回時，在陣列中填入的元素數目。</span><span class="sxs-lookup"><span data-stu-id="4ec29-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec29-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ec29-119">Return value</span></span>

<span data-ttu-id="4ec29-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ec29-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ec29-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4ec29-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4ec29-122">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="4ec29-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ec29-123">備註</span><span class="sxs-lookup"><span data-stu-id="4ec29-123">Remarks</span></span>

<span data-ttu-id="4ec29-124">**ID3DXConstantTable：： GetConstantDesc** 有時會傳回註冊計數為0的 [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) \_ 。</span><span class="sxs-lookup"><span data-stu-id="4ec29-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="4ec29-125">發生這種情況時，常數會出現在一個以上的暫存器 \_ 集中，但不會在該暫存器集合中配置任何空間。</span><span class="sxs-lookup"><span data-stu-id="4ec29-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="4ec29-126">因為取樣器可能在常數資料表中出現一次以上，所以這個方法可以傳回描述的陣列，每一個都有不同的暫存器索引。</span><span class="sxs-lookup"><span data-stu-id="4ec29-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec29-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ec29-127">Requirements</span></span>



| <span data-ttu-id="4ec29-128">需求</span><span class="sxs-lookup"><span data-stu-id="4ec29-128">Requirement</span></span> | <span data-ttu-id="4ec29-129">值</span><span class="sxs-lookup"><span data-stu-id="4ec29-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec29-130">標頭</span><span class="sxs-lookup"><span data-stu-id="4ec29-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4ec29-131"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ec29-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4ec29-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ec29-132">Library</span></span><br/> | <dl> <span data-ttu-id="4ec29-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ec29-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4ec29-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ec29-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec29-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="4ec29-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="4ec29-136">**ID3DXConstantTable::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="4ec29-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
