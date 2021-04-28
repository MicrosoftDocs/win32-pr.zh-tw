---
description: ID3DXBaseMesh：： GetVertexBuffer 方法-抓取與網格相關聯的頂點緩衝區。
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'ID3DXBaseMesh：： GetVertexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115366"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="551d2-103">ID3DXBaseMesh：： GetVertexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="551d2-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="551d2-104">抓取與網格相關聯的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="551d2-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="551d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="551d2-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="551d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="551d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="551d2-107">*ppVB* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="551d2-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="551d2-108">類型： **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="551d2-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="551d2-109">[**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)介面指標的位址，表示與網格相關聯的頂點緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="551d2-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="551d2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="551d2-110">Return value</span></span>

<span data-ttu-id="551d2-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="551d2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="551d2-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="551d2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="551d2-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="551d2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="551d2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="551d2-114">Requirements</span></span>



| <span data-ttu-id="551d2-115">需求</span><span class="sxs-lookup"><span data-stu-id="551d2-115">Requirement</span></span> | <span data-ttu-id="551d2-116">值</span><span class="sxs-lookup"><span data-stu-id="551d2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="551d2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="551d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="551d2-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="551d2-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="551d2-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="551d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="551d2-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="551d2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="551d2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="551d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551d2-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="551d2-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
