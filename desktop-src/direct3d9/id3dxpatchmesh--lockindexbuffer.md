---
description: 鎖定索引緩衝區。
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'ID3DXPatchMesh：： LockIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514713"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="f41e7-103">ID3DXPatchMesh：： LockIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="f41e7-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="f41e7-104">鎖定索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f41e7-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41e7-105">語法</span><span class="sxs-lookup"><span data-stu-id="f41e7-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="f41e7-106">參數</span><span class="sxs-lookup"><span data-stu-id="f41e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f41e7-107">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f41e7-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f41e7-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f41e7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f41e7-109">零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="f41e7-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="f41e7-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="f41e7-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="f41e7-111">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="f41e7-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="f41e7-112">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="f41e7-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="f41e7-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="f41e7-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="f41e7-114">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="f41e7-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="f41e7-115">如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。</span><span class="sxs-lookup"><span data-stu-id="f41e7-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="f41e7-116">*ppData* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="f41e7-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f41e7-117">類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f41e7-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f41e7-118">\*包含所傳回索引資料之記憶體緩衝區的 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="f41e7-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f41e7-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f41e7-119">Return value</span></span>

<span data-ttu-id="f41e7-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f41e7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f41e7-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f41e7-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f41e7-122">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="f41e7-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f41e7-123">備註</span><span class="sxs-lookup"><span data-stu-id="f41e7-123">Remarks</span></span>

<span data-ttu-id="f41e7-124">索引緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="f41e7-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="f41e7-125">Patch 網狀索引緩衝區是16位的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f41e7-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f41e7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f41e7-126">Requirements</span></span>



| <span data-ttu-id="f41e7-127">需求</span><span class="sxs-lookup"><span data-stu-id="f41e7-127">Requirement</span></span> | <span data-ttu-id="f41e7-128">值</span><span class="sxs-lookup"><span data-stu-id="f41e7-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f41e7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f41e7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f41e7-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f41e7-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f41e7-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="f41e7-131">Library</span></span><br/> | <dl> <span data-ttu-id="f41e7-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f41e7-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f41e7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f41e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f41e7-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="f41e7-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="f41e7-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="f41e7-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
