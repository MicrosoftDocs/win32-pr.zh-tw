---
description: 解除鎖定索引緩衝區。
ms.assetid: 69133f82-8391-4b7c-b39e-6730bc477b64
title: 'ID3DXBaseMesh：： UnlockIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2174735be8d9393c1b4ab4470fe360eeb040b0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981078"
---
# <a name="id3dxbasemeshunlockindexbuffer-method"></a><span data-ttu-id="f9d89-103">ID3DXBaseMesh：： UnlockIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="f9d89-103">ID3DXBaseMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="f9d89-104">解除鎖定索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f9d89-104">Unlocks an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d89-105">語法</span><span class="sxs-lookup"><span data-stu-id="f9d89-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="f9d89-106">參數</span><span class="sxs-lookup"><span data-stu-id="f9d89-106">Parameters</span></span>

<span data-ttu-id="f9d89-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f9d89-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9d89-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9d89-108">Return value</span></span>

<span data-ttu-id="f9d89-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9d89-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9d89-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f9d89-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9d89-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f9d89-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d89-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d89-112">Requirements</span></span>



| <span data-ttu-id="f9d89-113">需求</span><span class="sxs-lookup"><span data-stu-id="f9d89-113">Requirement</span></span> | <span data-ttu-id="f9d89-114">值</span><span class="sxs-lookup"><span data-stu-id="f9d89-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d89-115">標頭</span><span class="sxs-lookup"><span data-stu-id="f9d89-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f9d89-116"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d89-116"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f9d89-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="f9d89-117">Library</span></span><br/> | <dl> <span data-ttu-id="f9d89-118"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9d89-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f9d89-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9d89-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d89-120">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="f9d89-120">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 




