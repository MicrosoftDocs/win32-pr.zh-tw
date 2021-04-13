---
description: 限制可能影響頂點的骨骼數目，以及/或限制骨骼在頂點上可以有的影響數量。
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'ID3DX10SkinInfo：： Compact 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386440"
---
# <a name="id3dx10skininfocompact-method"></a><span data-ttu-id="636aa-103">ID3DX10SkinInfo：： Compact 方法</span><span class="sxs-lookup"><span data-stu-id="636aa-103">ID3DX10SkinInfo::Compact method</span></span>

<span data-ttu-id="636aa-104">限制可能影響頂點的骨骼數目，以及/或限制骨骼在頂點上可以有的影響數量。</span><span class="sxs-lookup"><span data-stu-id="636aa-104">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="636aa-105">語法</span><span class="sxs-lookup"><span data-stu-id="636aa-105">Syntax</span></span>


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a><span data-ttu-id="636aa-106">參數</span><span class="sxs-lookup"><span data-stu-id="636aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="636aa-107">*MaxPerVertexInfluences* \[在\]</span><span class="sxs-lookup"><span data-stu-id="636aa-107">*MaxPerVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="636aa-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636aa-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="636aa-109">可以影響任何指定頂點的最大骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="636aa-109">The maximum number of bones that can influence any given vertex.</span></span> <span data-ttu-id="636aa-110">如果這個值大於 [**ID3DX10SkinInfo：： GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)所傳回的值，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="636aa-110">This value is ignored if it is greater than the value returned by [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span></span>

</dd> <dt>

<span data-ttu-id="636aa-111">*ScaleMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="636aa-111">*ScaleMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="636aa-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="636aa-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="636aa-113">旗標，描述如何在某個頂點上的部分已由 MinWeight 切碎之後調整指定頂點上的剩餘權數。</span><span class="sxs-lookup"><span data-stu-id="636aa-113">A flag describing how to scale the remaining weights on a given vertex after some have been chopped off by MinWeight.</span></span> <span data-ttu-id="636aa-114">如果未 \_ 指定 D3DX10 SKININFO \_ ，就 \_ 不會調整加權。</span><span class="sxs-lookup"><span data-stu-id="636aa-114">If D3DX10\_SKININFO\_NO\_SCALING is specified, the weights will not be scaled at all.</span></span> <span data-ttu-id="636aa-115">如果 \_ \_ 指定了 D3DX10 SKININFO SCALE \_ TO \_ 1，則權數大於 MinWeight 將會相應增加，使其增加到1.0。</span><span class="sxs-lookup"><span data-stu-id="636aa-115">If D3DX10\_SKININFO\_SCALE\_TO\_1 is specified, the weights greater than MinWeight will be scaled up so that they add up to 1.0.</span></span> <span data-ttu-id="636aa-116">如果 \_ \_ 指定了 D3DX10 SKININFO SCALE \_ TO \_ TOTAL，則權數大於 MinWeight 將會相應增加，使其增加至原始總計。</span><span class="sxs-lookup"><span data-stu-id="636aa-116">If D3DX10\_SKININFO\_SCALE\_TO\_TOTAL is specified, the weights greater than MinWeight will be scaled up so that they add up to the original total.</span></span>

</dd> <dt>

<span data-ttu-id="636aa-117">*MinWeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="636aa-117">*MinWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="636aa-118">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="636aa-118">Type: **float**</span></span>

<span data-ttu-id="636aa-119">任何骨骼在任何頂點上可以有的影響（或權數）的最小百分比。</span><span class="sxs-lookup"><span data-stu-id="636aa-119">The minimum percentage of influence, or weight, that any bone can have on any vertex.</span></span> <span data-ttu-id="636aa-120">此值必須介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="636aa-120">This value must be between 0 and 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="636aa-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="636aa-121">Return value</span></span>

<span data-ttu-id="636aa-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="636aa-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="636aa-123">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="636aa-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="636aa-124">如果方法失敗，則傳回值可以是： E \_ OUTOFMEMORY 或 e \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="636aa-124">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="636aa-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="636aa-125">Requirements</span></span>



| <span data-ttu-id="636aa-126">需求</span><span class="sxs-lookup"><span data-stu-id="636aa-126">Requirement</span></span> | <span data-ttu-id="636aa-127">值</span><span class="sxs-lookup"><span data-stu-id="636aa-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="636aa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="636aa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="636aa-129"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="636aa-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="636aa-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="636aa-130">Library</span></span><br/> | <dl> <span data-ttu-id="636aa-131"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="636aa-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="636aa-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="636aa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636aa-133">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="636aa-133">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="636aa-134">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="636aa-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
