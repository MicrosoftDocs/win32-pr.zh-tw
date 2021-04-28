---
description: ID3DXBaseMesh：： GetIndexBuffer 方法-捕獲索引緩衝區中的資料。
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'ID3DXBaseMesh：： GetIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115426"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="d0355-103">ID3DXBaseMesh：： GetIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="d0355-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="d0355-104">抓取索引緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="d0355-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0355-105">語法</span><span class="sxs-lookup"><span data-stu-id="d0355-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="d0355-106">參數</span><span class="sxs-lookup"><span data-stu-id="d0355-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0355-107">*ppIB* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="d0355-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d0355-108">類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="d0355-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="d0355-109">[**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面指標的位址，表示與網格相關聯的索引緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="d0355-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0355-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0355-110">Return value</span></span>

<span data-ttu-id="d0355-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0355-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0355-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d0355-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0355-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d0355-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0355-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0355-114">Requirements</span></span>



| <span data-ttu-id="d0355-115">需求</span><span class="sxs-lookup"><span data-stu-id="d0355-115">Requirement</span></span> | <span data-ttu-id="d0355-116">值</span><span class="sxs-lookup"><span data-stu-id="d0355-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0355-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d0355-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d0355-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0355-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d0355-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0355-119">Library</span></span><br/> | <dl> <span data-ttu-id="d0355-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0355-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0355-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0355-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0355-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d0355-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
