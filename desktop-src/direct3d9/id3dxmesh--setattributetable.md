---
description: 設定網格的屬性工作表和儲存在資料表中的專案數目。
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'ID3DXMesh：： SetAttributeTable 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986730"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="00528-103">ID3DXMesh：： SetAttributeTable 方法</span><span class="sxs-lookup"><span data-stu-id="00528-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="00528-104">設定網格的屬性工作表和儲存在資料表中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="00528-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="00528-105">語法</span><span class="sxs-lookup"><span data-stu-id="00528-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="00528-106">參數</span><span class="sxs-lookup"><span data-stu-id="00528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00528-107">*pAttribTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00528-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00528-108">Type： **Const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="00528-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="00528-109">[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)結構陣列的指標，表示網格屬性工作表中的專案。</span><span class="sxs-lookup"><span data-stu-id="00528-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="00528-110">*cAttribTableSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00528-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00528-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00528-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00528-112">網格屬性工作表中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="00528-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00528-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="00528-113">Return value</span></span>

<span data-ttu-id="00528-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00528-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00528-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="00528-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="00528-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="00528-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="00528-117">備註</span><span class="sxs-lookup"><span data-stu-id="00528-117">Remarks</span></span>

<span data-ttu-id="00528-118">如果應用程式會追蹤屬性工作表中的資訊，並重新排列資料表，使其成為屬性或臉部變更的結果，此方法可讓應用程式更新屬性工作表，而不是再次呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 。</span><span class="sxs-lookup"><span data-stu-id="00528-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="00528-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="00528-119">Requirements</span></span>



| <span data-ttu-id="00528-120">需求</span><span class="sxs-lookup"><span data-stu-id="00528-120">Requirement</span></span> | <span data-ttu-id="00528-121">值</span><span class="sxs-lookup"><span data-stu-id="00528-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00528-122">標頭</span><span class="sxs-lookup"><span data-stu-id="00528-122">Header</span></span><br/>  | <dl> <span data-ttu-id="00528-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="00528-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="00528-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="00528-124">Library</span></span><br/> | <dl> <span data-ttu-id="00528-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00528-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00528-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00528-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00528-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="00528-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="00528-128">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="00528-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="00528-129">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="00528-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
