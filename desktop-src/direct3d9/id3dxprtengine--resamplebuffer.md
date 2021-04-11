---
description: Resamples 輸入 ID3DXPRTBuffer 緩衝區，並將其儲存至輸出緩衝區。 這個方法可以用來將頂點緩衝區轉換成材質緩衝區，反之亦然。 它也可以用來將單一通道緩衝區轉換成3通道緩衝區，反之亦然。
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine：： ResampleBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696804"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="49728-105">ID3DXPRTEngine：： ResampleBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="49728-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="49728-106">Resamples 輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區，並將其儲存至輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="49728-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="49728-107">這個方法可以用來將頂點緩衝區轉換成材質緩衝區，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="49728-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="49728-108">它也可以用來將單一通道緩衝區轉換成3通道緩衝區，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="49728-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="49728-109">語法</span><span class="sxs-lookup"><span data-stu-id="49728-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="49728-110">參數</span><span class="sxs-lookup"><span data-stu-id="49728-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49728-111">*pBufferIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49728-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49728-112">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="49728-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="49728-113">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="49728-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="49728-114">*pBufferOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="49728-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49728-115">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="49728-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="49728-116">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="49728-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49728-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="49728-117">Return value</span></span>

<span data-ttu-id="49728-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49728-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49728-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="49728-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49728-120">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="49728-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="49728-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="49728-121">Requirements</span></span>



| <span data-ttu-id="49728-122">需求</span><span class="sxs-lookup"><span data-stu-id="49728-122">Requirement</span></span> | <span data-ttu-id="49728-123">值</span><span class="sxs-lookup"><span data-stu-id="49728-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49728-124">標頭</span><span class="sxs-lookup"><span data-stu-id="49728-124">Header</span></span><br/>  | <dl> <span data-ttu-id="49728-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="49728-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="49728-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="49728-126">Library</span></span><br/> | <dl> <span data-ttu-id="49728-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="49728-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49728-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49728-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49728-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="49728-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




