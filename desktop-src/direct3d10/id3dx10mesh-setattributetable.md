---
description: ID3DX10Mesh：： SetAttributeTable 方法：設定網格的屬性資料表和儲存在資料表中的專案數目。
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'ID3DX10Mesh：： SetAttributeTable 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084006"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="a8b57-103">ID3DX10Mesh：： SetAttributeTable 方法</span><span class="sxs-lookup"><span data-stu-id="a8b57-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="a8b57-104">設定網格的屬性工作表和儲存在資料表中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="a8b57-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b57-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8b57-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="a8b57-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8b57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b57-107">*pAttribTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8b57-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b57-108">Type： **Const [**D3DX10 \_ 屬性 \_ 範圍**](d3dx10-attribute-range.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8b57-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="a8b57-109">D3DX10 \_ 屬性範圍結構的陣列指標 \_ ，表示網格屬性工作表中的專案。</span><span class="sxs-lookup"><span data-stu-id="a8b57-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="a8b57-110">*cAttribTableSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8b57-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b57-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8b57-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8b57-112">網格屬性工作表中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="a8b57-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b57-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8b57-113">Return value</span></span>

<span data-ttu-id="a8b57-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8b57-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8b57-115">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a8b57-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b57-116">備註</span><span class="sxs-lookup"><span data-stu-id="a8b57-116">Remarks</span></span>

<span data-ttu-id="a8b57-117">如果應用程式會追蹤屬性工作表中的資訊，並重新排列資料表，使其成為屬性或臉部變更的結果，此方法可讓應用程式更新屬性工作表，而不是再次呼叫 ID3DX10Mesh：： Optimize。</span><span class="sxs-lookup"><span data-stu-id="a8b57-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b57-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8b57-118">Requirements</span></span>



| <span data-ttu-id="a8b57-119">需求</span><span class="sxs-lookup"><span data-stu-id="a8b57-119">Requirement</span></span> | <span data-ttu-id="a8b57-120">值</span><span class="sxs-lookup"><span data-stu-id="a8b57-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b57-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a8b57-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b57-122"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b57-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8b57-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8b57-123">Library</span></span><br/> | <dl> <span data-ttu-id="a8b57-124"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8b57-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b57-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8b57-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b57-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="a8b57-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="a8b57-127">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a8b57-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
