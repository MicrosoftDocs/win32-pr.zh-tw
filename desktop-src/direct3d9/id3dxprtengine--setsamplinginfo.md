---
description: 設定預先計算 radiance 傳輸 (PRT) 模擬器所使用的取樣屬性。
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine：： SetSamplingInfo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696695"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a><span data-ttu-id="9564e-103">ID3DXPRTEngine：： SetSamplingInfo 方法</span><span class="sxs-lookup"><span data-stu-id="9564e-103">ID3DXPRTEngine::SetSamplingInfo method</span></span>

<span data-ttu-id="9564e-104">設定預先計算 radiance 傳輸 (PRT) 模擬器所使用的取樣屬性。</span><span class="sxs-lookup"><span data-stu-id="9564e-104">Sets sampling properties used by the precomputed radiance transfer (PRT) simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="9564e-105">語法</span><span class="sxs-lookup"><span data-stu-id="9564e-105">Syntax</span></span>


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a><span data-ttu-id="9564e-106">參數</span><span class="sxs-lookup"><span data-stu-id="9564e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9564e-107">*NumRays* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9564e-107">*NumRays* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9564e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9564e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9564e-109">要在每個樣本上導向的光線數量。</span><span class="sxs-lookup"><span data-stu-id="9564e-109">Number of light rays to direct at each sample.</span></span> <span data-ttu-id="9564e-110">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="9564e-110">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="9564e-111">*UseSphere* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9564e-111">*UseSphere* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9564e-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9564e-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9564e-113">若 **為 TRUE**，將會針對整個球體計算範例。</span><span class="sxs-lookup"><span data-stu-id="9564e-113">If **TRUE**, samples will be computed over a full sphere.</span></span> <span data-ttu-id="9564e-114">如果 **為 FALSE**，則會透過半球計算範例。</span><span class="sxs-lookup"><span data-stu-id="9564e-114">If **FALSE**, samples will be computed over a hemisphere.</span></span>

</dd> <dt>

<span data-ttu-id="9564e-115">*UseCosine* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9564e-115">*UseCosine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9564e-116">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9564e-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9564e-117">若 **為 TRUE，則** 使用範例的余弦加權。</span><span class="sxs-lookup"><span data-stu-id="9564e-117">If **TRUE**, use a cosine weighting of samples.</span></span> <span data-ttu-id="9564e-118">如果 UseCosine 和 UseSphere 都是 **TRUE**，方法將會失敗，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9564e-118">If both UseCosine and UseSphere are **TRUE**, the method will fail and an error will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="9564e-119">*適應性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9564e-119">*Adaptive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9564e-120">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9564e-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9564e-121">必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9564e-121">Must be **FALSE**.</span></span> <span data-ttu-id="9564e-122">彈性取樣目前未執行。</span><span class="sxs-lookup"><span data-stu-id="9564e-122">Adaptive sampling is currently not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="9564e-123">*AdaptiveThresh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9564e-123">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9564e-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9564e-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9564e-125">忽略。</span><span class="sxs-lookup"><span data-stu-id="9564e-125">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9564e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="9564e-126">Return value</span></span>

<span data-ttu-id="9564e-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9564e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9564e-128">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9564e-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9564e-129">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、e \_ >notimpl、e \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="9564e-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9564e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9564e-130">Requirements</span></span>



| <span data-ttu-id="9564e-131">需求</span><span class="sxs-lookup"><span data-stu-id="9564e-131">Requirement</span></span> | <span data-ttu-id="9564e-132">值</span><span class="sxs-lookup"><span data-stu-id="9564e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9564e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="9564e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9564e-134"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="9564e-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9564e-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="9564e-135">Library</span></span><br/> | <dl> <span data-ttu-id="9564e-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9564e-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9564e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9564e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9564e-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9564e-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
