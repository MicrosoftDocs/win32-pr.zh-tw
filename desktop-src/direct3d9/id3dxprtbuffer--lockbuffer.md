---
description: 鎖定某個範圍的頂點或材質範例資料，並取得緩衝區記憶體中位置的指標。
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'ID3DXPRTBuffer：： LockBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981255"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="b67f6-103">ID3DXPRTBuffer：： LockBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="b67f6-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="b67f6-104">鎖定某個範圍的頂點或材質範例資料，並取得緩衝區記憶體中位置的指標。</span><span class="sxs-lookup"><span data-stu-id="b67f6-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b67f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b67f6-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="b67f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="b67f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b67f6-107">*開始* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b67f6-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67f6-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b67f6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b67f6-109">頂點或材質資料範例的索引。</span><span class="sxs-lookup"><span data-stu-id="b67f6-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="b67f6-110">*NumSamples* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b67f6-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67f6-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b67f6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b67f6-112">取樣 (或材質) 的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="b67f6-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="b67f6-113">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b67f6-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b67f6-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b67f6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="b67f6-115">記憶體中開始範例開始位置的位置指標。</span><span class="sxs-lookup"><span data-stu-id="b67f6-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="b67f6-116">緩衝區資料的記憶體配置為：</span><span class="sxs-lookup"><span data-stu-id="b67f6-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b67f6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b67f6-117">Return value</span></span>

<span data-ttu-id="b67f6-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b67f6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b67f6-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b67f6-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b67f6-120">如果方法失敗，則會傳回下列值：</span><span class="sxs-lookup"><span data-stu-id="b67f6-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="b67f6-121">備註</span><span class="sxs-lookup"><span data-stu-id="b67f6-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b67f6-122">需求</span><span class="sxs-lookup"><span data-stu-id="b67f6-122">Requirements</span></span>



| <span data-ttu-id="b67f6-123">需求</span><span class="sxs-lookup"><span data-stu-id="b67f6-123">Requirement</span></span> | <span data-ttu-id="b67f6-124">值</span><span class="sxs-lookup"><span data-stu-id="b67f6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b67f6-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b67f6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b67f6-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b67f6-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b67f6-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="b67f6-127">Library</span></span><br/> | <dl> <span data-ttu-id="b67f6-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b67f6-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b67f6-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b67f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67f6-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="b67f6-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="b67f6-131">**ID3DXPRTBuffer::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="b67f6-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="b67f6-132">**ID3DXPRTBuffer::GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="b67f6-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="b67f6-133">**ID3DXPRTBuffer::GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="b67f6-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
