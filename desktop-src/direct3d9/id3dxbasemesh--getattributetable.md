---
description: 抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'ID3DXBaseMesh：： GetAttributeTable 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70c93c8f477655200418793f53706731b42a47ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976501"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="8d45e-103">ID3DXBaseMesh：： GetAttributeTable 方法</span><span class="sxs-lookup"><span data-stu-id="8d45e-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="8d45e-104">抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。</span><span class="sxs-lookup"><span data-stu-id="8d45e-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d45e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8d45e-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="8d45e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8d45e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d45e-107">*pAttribTable* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8d45e-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d45e-108">類型： **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d45e-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="8d45e-109">[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)結構陣列的指標，代表網格屬性工作表中的專案。</span><span class="sxs-lookup"><span data-stu-id="8d45e-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="8d45e-110">指定 **Null** 可取出 pAttribTableSize 的值。</span><span class="sxs-lookup"><span data-stu-id="8d45e-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="8d45e-111">*pAttribTableSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8d45e-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d45e-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d45e-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d45e-113">儲存在 pAttribTable 中的專案數或要填入的值的指標，該專案是以網格的屬性工作表中儲存的專案數來填滿。</span><span class="sxs-lookup"><span data-stu-id="8d45e-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d45e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d45e-114">Return value</span></span>

<span data-ttu-id="8d45e-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d45e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d45e-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8d45e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d45e-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="8d45e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d45e-118">備註</span><span class="sxs-lookup"><span data-stu-id="8d45e-118">Remarks</span></span>

<span data-ttu-id="8d45e-119">屬性資料表是由 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) 和傳遞 D3DXMESHOPT ATTRSORT 的 \_ 旗標參數所建立。</span><span class="sxs-lookup"><span data-stu-id="8d45e-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="8d45e-120">屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。</span><span class="sxs-lookup"><span data-stu-id="8d45e-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="8d45e-121">此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時繪製指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d45e-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d45e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d45e-122">Requirements</span></span>



| <span data-ttu-id="8d45e-123">需求</span><span class="sxs-lookup"><span data-stu-id="8d45e-123">Requirement</span></span> | <span data-ttu-id="8d45e-124">值</span><span class="sxs-lookup"><span data-stu-id="8d45e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d45e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8d45e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8d45e-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d45e-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8d45e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d45e-127">Library</span></span><br/> | <dl> <span data-ttu-id="8d45e-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d45e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d45e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d45e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d45e-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="8d45e-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
