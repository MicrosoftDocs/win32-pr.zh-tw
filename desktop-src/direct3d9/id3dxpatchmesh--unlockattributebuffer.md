---
description: 解除鎖定屬性緩衝區。
ms.assetid: 4077ad15-9753-4031-81e7-c04e4267a0c9
title: 'ID3DXPatchMesh：： UnlockAttributeBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 42ea5ffacae2a2de073f6c16a9d29a7f76633ef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988223"
---
# <a name="id3dxpatchmeshunlockattributebuffer-method"></a><span data-ttu-id="83a02-103">ID3DXPatchMesh：： UnlockAttributeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="83a02-103">ID3DXPatchMesh::UnlockAttributeBuffer method</span></span>

<span data-ttu-id="83a02-104">解除鎖定屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="83a02-104">Unlock the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="83a02-105">語法</span><span class="sxs-lookup"><span data-stu-id="83a02-105">Syntax</span></span>


```C++
HRESULT UnlockAttributeBuffer();
```



## <a name="parameters"></a><span data-ttu-id="83a02-106">參數</span><span class="sxs-lookup"><span data-stu-id="83a02-106">Parameters</span></span>

<span data-ttu-id="83a02-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="83a02-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83a02-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="83a02-108">Return value</span></span>

<span data-ttu-id="83a02-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83a02-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83a02-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="83a02-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83a02-111">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="83a02-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="83a02-112">備註</span><span class="sxs-lookup"><span data-stu-id="83a02-112">Remarks</span></span>

<span data-ttu-id="83a02-113">屬性緩衝區通常會鎖定、寫入，然後解除鎖定以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="83a02-113">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a02-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="83a02-114">Requirements</span></span>



| <span data-ttu-id="83a02-115">需求</span><span class="sxs-lookup"><span data-stu-id="83a02-115">Requirement</span></span> | <span data-ttu-id="83a02-116">值</span><span class="sxs-lookup"><span data-stu-id="83a02-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83a02-117">標頭</span><span class="sxs-lookup"><span data-stu-id="83a02-117">Header</span></span><br/>  | <dl> <span data-ttu-id="83a02-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="83a02-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="83a02-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="83a02-119">Library</span></span><br/> | <dl> <span data-ttu-id="83a02-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="83a02-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83a02-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83a02-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a02-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="83a02-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




