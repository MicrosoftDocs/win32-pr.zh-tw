---
description: 鎖定頂點緩衝區，並取得頂點緩衝區記憶體的指標。
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh：： LockVertexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976494"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="d05bd-103">ID3DXBaseMesh：： LockVertexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="d05bd-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="d05bd-104">鎖定頂點緩衝區，並取得頂點緩衝區記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="d05bd-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d05bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="d05bd-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="d05bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="d05bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05bd-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d05bd-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d05bd-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d05bd-109">零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="d05bd-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="d05bd-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="d05bd-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="d05bd-111">D3DLOCK \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="d05bd-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="d05bd-112">D3DLOCK \_ 沒有 \_ 中途 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="d05bd-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="d05bd-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="d05bd-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="d05bd-114">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="d05bd-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="d05bd-115">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="d05bd-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="d05bd-116">如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。</span><span class="sxs-lookup"><span data-stu-id="d05bd-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d05bd-117">*ppData* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="d05bd-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d05bd-118">類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d05bd-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d05bd-119">\*包含頂點資料之緩衝區的 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="d05bd-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05bd-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d05bd-120">Return value</span></span>

<span data-ttu-id="d05bd-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d05bd-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d05bd-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d05bd-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d05bd-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d05bd-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d05bd-124">備註</span><span class="sxs-lookup"><span data-stu-id="d05bd-124">Remarks</span></span>

<span data-ttu-id="d05bd-125">使用頂點緩衝區時，您可以進行多次鎖定呼叫;不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。</span><span class="sxs-lookup"><span data-stu-id="d05bd-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="d05bd-126">任何目前設定的頂點緩衝區上的任何未完成鎖定計數，DrawPrimitive 呼叫都不會成功。</span><span class="sxs-lookup"><span data-stu-id="d05bd-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05bd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d05bd-127">Requirements</span></span>



| <span data-ttu-id="d05bd-128">需求</span><span class="sxs-lookup"><span data-stu-id="d05bd-128">Requirement</span></span> | <span data-ttu-id="d05bd-129">值</span><span class="sxs-lookup"><span data-stu-id="d05bd-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d05bd-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d05bd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d05bd-131"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d05bd-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="d05bd-132">Library</span></span><br/> | <dl> <span data-ttu-id="d05bd-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d05bd-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d05bd-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d05bd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05bd-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d05bd-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
