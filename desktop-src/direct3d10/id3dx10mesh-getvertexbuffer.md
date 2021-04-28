---
description: ID3DX10Mesh：： GetVertexBuffer 方法-抓取與網格相關聯的頂點緩衝區。
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'ID3DX10Mesh：： GetVertexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108076"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="38a80-103">ID3DX10Mesh：： GetVertexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="38a80-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="38a80-104">抓取與網格相關聯的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="38a80-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a80-105">語法</span><span class="sxs-lookup"><span data-stu-id="38a80-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="38a80-106">參數</span><span class="sxs-lookup"><span data-stu-id="38a80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a80-107">*windows.storage.streams.ibuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38a80-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a80-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38a80-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38a80-109">要取得的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="38a80-109">The vertex buffer to get.</span></span> <span data-ttu-id="38a80-110">這是索引值。</span><span class="sxs-lookup"><span data-stu-id="38a80-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="38a80-111">*ppVertexBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="38a80-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38a80-112">類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="38a80-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="38a80-113">頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="38a80-113">The vertex buffer.</span></span> <span data-ttu-id="38a80-114">請參閱 [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="38a80-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a80-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="38a80-115">Return value</span></span>

<span data-ttu-id="38a80-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38a80-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38a80-117">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="38a80-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38a80-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="38a80-118">Requirements</span></span>



| <span data-ttu-id="38a80-119">需求</span><span class="sxs-lookup"><span data-stu-id="38a80-119">Requirement</span></span> | <span data-ttu-id="38a80-120">值</span><span class="sxs-lookup"><span data-stu-id="38a80-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38a80-121">標頭</span><span class="sxs-lookup"><span data-stu-id="38a80-121">Header</span></span><br/>  | <dl> <span data-ttu-id="38a80-122"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="38a80-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="38a80-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="38a80-123">Library</span></span><br/> | <dl> <span data-ttu-id="38a80-124"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="38a80-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a80-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38a80-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a80-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="38a80-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="38a80-127">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="38a80-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
