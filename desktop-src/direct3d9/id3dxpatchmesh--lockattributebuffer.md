---
description: 鎖定屬性緩衝區。
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'ID3DXPatchMesh：： LockAttributeBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988625"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="78ba1-103">ID3DXPatchMesh：： LockAttributeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="78ba1-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="78ba1-104">鎖定屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="78ba1-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ba1-105">語法</span><span class="sxs-lookup"><span data-stu-id="78ba1-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="78ba1-106">參數</span><span class="sxs-lookup"><span data-stu-id="78ba1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78ba1-107">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78ba1-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78ba1-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78ba1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78ba1-109">零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="78ba1-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="78ba1-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="78ba1-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="78ba1-111">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="78ba1-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="78ba1-112">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="78ba1-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="78ba1-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="78ba1-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="78ba1-114">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="78ba1-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="78ba1-115">如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。</span><span class="sxs-lookup"><span data-stu-id="78ba1-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="78ba1-116">*ppData* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="78ba1-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="78ba1-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="78ba1-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="78ba1-118">緩衝區指標的位址，其中包含網格中每個臉部的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="78ba1-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78ba1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="78ba1-119">Return value</span></span>

<span data-ttu-id="78ba1-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78ba1-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78ba1-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="78ba1-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78ba1-122">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="78ba1-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78ba1-123">備註</span><span class="sxs-lookup"><span data-stu-id="78ba1-123">Remarks</span></span>

<span data-ttu-id="78ba1-124">屬性緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="78ba1-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="78ba1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="78ba1-125">Requirements</span></span>



| <span data-ttu-id="78ba1-126">需求</span><span class="sxs-lookup"><span data-stu-id="78ba1-126">Requirement</span></span> | <span data-ttu-id="78ba1-127">值</span><span class="sxs-lookup"><span data-stu-id="78ba1-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78ba1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="78ba1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="78ba1-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="78ba1-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78ba1-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="78ba1-130">Library</span></span><br/> | <dl> <span data-ttu-id="78ba1-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="78ba1-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78ba1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78ba1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ba1-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="78ba1-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
