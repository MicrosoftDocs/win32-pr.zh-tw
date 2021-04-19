---
description: 鎖定包含網格屬性資料的網狀緩衝區，並傳回其指標。
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh：： LockAttributeBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998998"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="91735-103">ID3DXMesh：： LockAttributeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="91735-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="91735-104">鎖定包含網格屬性資料的網狀緩衝區，並傳回其指標。</span><span class="sxs-lookup"><span data-stu-id="91735-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="91735-105">語法</span><span class="sxs-lookup"><span data-stu-id="91735-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="91735-106">參數</span><span class="sxs-lookup"><span data-stu-id="91735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91735-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="91735-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91735-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91735-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91735-109">零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="91735-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="91735-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="91735-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="91735-111">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="91735-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="91735-112">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="91735-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="91735-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="91735-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="91735-114">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="91735-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="91735-115">如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。</span><span class="sxs-lookup"><span data-stu-id="91735-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="91735-116">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="91735-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91735-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="91735-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="91735-118">緩衝區指標的位址，其中包含網格中每個臉部的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="91735-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91735-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="91735-119">Return value</span></span>

<span data-ttu-id="91735-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91735-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91735-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="91735-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="91735-122">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="91735-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="91735-123">備註</span><span class="sxs-lookup"><span data-stu-id="91735-123">Remarks</span></span>

<span data-ttu-id="91735-124">如果已呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) ，則網格也會有可使用 [**ID3DXBaseMesh：： GetAttributeTable**](id3dxbasemesh--getattributetable.md) 方法存取的屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="91735-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91735-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="91735-125">Requirements</span></span>



| <span data-ttu-id="91735-126">需求</span><span class="sxs-lookup"><span data-stu-id="91735-126">Requirement</span></span> | <span data-ttu-id="91735-127">值</span><span class="sxs-lookup"><span data-stu-id="91735-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91735-128">標頭</span><span class="sxs-lookup"><span data-stu-id="91735-128">Header</span></span><br/>  | <dl> <span data-ttu-id="91735-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="91735-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="91735-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="91735-130">Library</span></span><br/> | <dl> <span data-ttu-id="91735-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91735-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91735-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91735-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91735-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="91735-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="91735-134">**ID3DXMesh::UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="91735-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="91735-135">**ID3DXBaseMesh::GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="91735-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="91735-136">**ID3DXMesh::SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="91735-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
