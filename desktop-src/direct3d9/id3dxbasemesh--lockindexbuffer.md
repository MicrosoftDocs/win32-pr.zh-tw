---
description: 鎖定索引緩衝區，並取得索引緩衝區記憶體的指標。
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh：： LockIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035328"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="6a7cf-103">ID3DXBaseMesh：： LockIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="6a7cf-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="6a7cf-104">鎖定索引緩衝區，並取得索引緩衝區記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a7cf-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="6a7cf-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a7cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a7cf-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6a7cf-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7cf-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a7cf-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a7cf-109">零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="6a7cf-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="6a7cf-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="6a7cf-111">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="6a7cf-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="6a7cf-112">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="6a7cf-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="6a7cf-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="6a7cf-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="6a7cf-114">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="6a7cf-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="6a7cf-115">如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a7cf-116">*ppData* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="6a7cf-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7cf-117">類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a7cf-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6a7cf-118">\*包含索引資料之緩衝區的 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="6a7cf-119">此緩衝區中的索引計數會等於 [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a7cf-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a7cf-120">Return value</span></span>

<span data-ttu-id="6a7cf-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a7cf-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a7cf-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a7cf-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a7cf-124">備註</span><span class="sxs-lookup"><span data-stu-id="6a7cf-124">Remarks</span></span>

<span data-ttu-id="6a7cf-125">使用索引緩衝區時，您可以進行多個鎖定呼叫。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="6a7cf-126">不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="6a7cf-127">任何目前設定的索引緩衝區上的任何未完成鎖定計數，DrawPrimitive 呼叫都不會成功。</span><span class="sxs-lookup"><span data-stu-id="6a7cf-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a7cf-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a7cf-128">Requirements</span></span>



| <span data-ttu-id="6a7cf-129">需求</span><span class="sxs-lookup"><span data-stu-id="6a7cf-129">Requirement</span></span> | <span data-ttu-id="6a7cf-130">值</span><span class="sxs-lookup"><span data-stu-id="6a7cf-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7cf-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6a7cf-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6a7cf-132"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a7cf-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6a7cf-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a7cf-133">Library</span></span><br/> | <dl> <span data-ttu-id="6a7cf-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a7cf-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a7cf-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a7cf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7cf-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="6a7cf-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
