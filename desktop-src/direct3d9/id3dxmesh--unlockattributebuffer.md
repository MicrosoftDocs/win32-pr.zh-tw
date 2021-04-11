---
description: 解除鎖定屬性緩衝區。
ms.assetid: 47d59cf4-3497-4fee-b456-11c7fad84c66
title: 'ID3DXMesh：： UnlockAttributeBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.UnlockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 73be55bf6893f0191c6afa722caf389f3ae005d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196421"
---
# <a name="id3dxmeshunlockattributebuffer-method"></a><span data-ttu-id="2c135-103">ID3DXMesh：： UnlockAttributeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="2c135-103">ID3DXMesh::UnlockAttributeBuffer method</span></span>

<span data-ttu-id="2c135-104">解除鎖定屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2c135-104">Unlocks an attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c135-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c135-105">Syntax</span></span>


```C++
HRESULT UnlockAttributeBuffer();
```



## <a name="parameters"></a><span data-ttu-id="2c135-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c135-106">Parameters</span></span>

<span data-ttu-id="2c135-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2c135-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c135-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c135-108">Return value</span></span>

<span data-ttu-id="2c135-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c135-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c135-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2c135-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c135-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2c135-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c135-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c135-112">Requirements</span></span>



| <span data-ttu-id="2c135-113">需求</span><span class="sxs-lookup"><span data-stu-id="2c135-113">Requirement</span></span> | <span data-ttu-id="2c135-114">值</span><span class="sxs-lookup"><span data-stu-id="2c135-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c135-115">標頭</span><span class="sxs-lookup"><span data-stu-id="2c135-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2c135-116"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c135-116"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2c135-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c135-117">Library</span></span><br/> | <dl> <span data-ttu-id="2c135-118"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c135-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2c135-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c135-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c135-120">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="2c135-120">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="2c135-121">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="2c135-121">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> </dl>

 

 




