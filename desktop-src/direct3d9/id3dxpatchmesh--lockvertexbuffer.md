---
description: 鎖定頂點緩衝區。
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'ID3DXPatchMesh：： LockVertexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854035"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="e07d0-103">ID3DXPatchMesh：： LockVertexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="e07d0-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="e07d0-104">鎖定頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e07d0-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="e07d0-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="e07d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e07d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07d0-107">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e07d0-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07d0-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e07d0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e07d0-109">零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="e07d0-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="e07d0-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="e07d0-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="e07d0-111">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="e07d0-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="e07d0-112">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="e07d0-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="e07d0-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="e07d0-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="e07d0-114">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="e07d0-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="e07d0-115">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="e07d0-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="e07d0-116">如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。</span><span class="sxs-lookup"><span data-stu-id="e07d0-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="e07d0-117">*ppData* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="e07d0-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e07d0-118">類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e07d0-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e07d0-119">\*包含所傳回頂點資料之記憶體緩衝區的 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="e07d0-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07d0-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e07d0-120">Return value</span></span>

<span data-ttu-id="e07d0-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e07d0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e07d0-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e07d0-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e07d0-123">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e07d0-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e07d0-124">備註</span><span class="sxs-lookup"><span data-stu-id="e07d0-124">Remarks</span></span>

<span data-ttu-id="e07d0-125">頂點緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="e07d0-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="e07d0-126">Patch 網格使用16位索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e07d0-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e07d0-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e07d0-127">Requirements</span></span>



| <span data-ttu-id="e07d0-128">需求</span><span class="sxs-lookup"><span data-stu-id="e07d0-128">Requirement</span></span> | <span data-ttu-id="e07d0-129">值</span><span class="sxs-lookup"><span data-stu-id="e07d0-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e07d0-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e07d0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e07d0-131"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e07d0-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e07d0-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="e07d0-132">Library</span></span><br/> | <dl> <span data-ttu-id="e07d0-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e07d0-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e07d0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e07d0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07d0-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="e07d0-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
