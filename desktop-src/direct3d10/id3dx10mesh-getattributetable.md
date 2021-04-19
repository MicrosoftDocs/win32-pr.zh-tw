---
description: 抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh：： GetAttributeTable 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986530"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="a1fca-103">ID3DX10Mesh：： GetAttributeTable 方法</span><span class="sxs-lookup"><span data-stu-id="a1fca-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="a1fca-104">抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。</span><span class="sxs-lookup"><span data-stu-id="a1fca-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1fca-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1fca-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="a1fca-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1fca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1fca-107">*pAttribTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1fca-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1fca-108">Type： **[ **D3DX10 \_ 屬性 \_ 範圍**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1fca-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="a1fca-109">D3DX10 \_ 屬性範圍結構的陣列指標 \_ ，表示網格屬性工作表中的專案。</span><span class="sxs-lookup"><span data-stu-id="a1fca-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="a1fca-110">指定 **Null** 可取出 pAttribTableSize 的值。</span><span class="sxs-lookup"><span data-stu-id="a1fca-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="a1fca-111">*pAttribTableSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1fca-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1fca-112">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1fca-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1fca-113">儲存在 pAttribTable 中的專案數或要填入的值的指標，該專案是以網格的屬性工作表中儲存的專案數來填滿。</span><span class="sxs-lookup"><span data-stu-id="a1fca-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1fca-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1fca-114">Return value</span></span>

<span data-ttu-id="a1fca-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1fca-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1fca-116">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a1fca-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1fca-117">備註</span><span class="sxs-lookup"><span data-stu-id="a1fca-117">Remarks</span></span>

<span data-ttu-id="a1fca-118">屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。</span><span class="sxs-lookup"><span data-stu-id="a1fca-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="a1fca-119">此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時繪製指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1fca-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1fca-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1fca-120">Requirements</span></span>



| <span data-ttu-id="a1fca-121">需求</span><span class="sxs-lookup"><span data-stu-id="a1fca-121">Requirement</span></span> | <span data-ttu-id="a1fca-122">值</span><span class="sxs-lookup"><span data-stu-id="a1fca-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1fca-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a1fca-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a1fca-124"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1fca-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1fca-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1fca-125">Library</span></span><br/> | <dl> <span data-ttu-id="a1fca-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1fca-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1fca-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1fca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1fca-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="a1fca-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="a1fca-129">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a1fca-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
