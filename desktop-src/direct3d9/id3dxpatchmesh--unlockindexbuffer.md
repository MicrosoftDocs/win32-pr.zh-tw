---
description: 解除鎖定索引緩衝區。
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'ID3DXPatchMesh：： UnlockIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9bae54c6c4477682422328410558f1b405eb2677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976504"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a><span data-ttu-id="6800e-103">ID3DXPatchMesh：： UnlockIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="6800e-103">ID3DXPatchMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="6800e-104">解除鎖定索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6800e-104">Unlock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6800e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6800e-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="6800e-106">參數</span><span class="sxs-lookup"><span data-stu-id="6800e-106">Parameters</span></span>

<span data-ttu-id="6800e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6800e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6800e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6800e-108">Return value</span></span>

<span data-ttu-id="6800e-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6800e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6800e-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6800e-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6800e-111">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6800e-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6800e-112">備註</span><span class="sxs-lookup"><span data-stu-id="6800e-112">Remarks</span></span>

<span data-ttu-id="6800e-113">索引緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="6800e-113">The index buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="6800e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6800e-114">Requirements</span></span>



| <span data-ttu-id="6800e-115">需求</span><span class="sxs-lookup"><span data-stu-id="6800e-115">Requirement</span></span> | <span data-ttu-id="6800e-116">值</span><span class="sxs-lookup"><span data-stu-id="6800e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6800e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6800e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6800e-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6800e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6800e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6800e-119">Library</span></span><br/> | <dl> <span data-ttu-id="6800e-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6800e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6800e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6800e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6800e-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="6800e-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




