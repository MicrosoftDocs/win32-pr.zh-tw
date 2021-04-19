---
description: 繪製網格的子集。
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: 'ID3DX10Mesh：:D rawSubset 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976706"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="35577-103">ID3DX10Mesh：:D rawSubset 方法</span><span class="sxs-lookup"><span data-stu-id="35577-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="35577-104">繪製網格的子集。</span><span class="sxs-lookup"><span data-stu-id="35577-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="35577-105">語法</span><span class="sxs-lookup"><span data-stu-id="35577-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="35577-106">參數</span><span class="sxs-lookup"><span data-stu-id="35577-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35577-107">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35577-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35577-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35577-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35577-109">指定要繪製的網格子集。</span><span class="sxs-lookup"><span data-stu-id="35577-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="35577-110">此值可用來區分網格中的臉部，以屬於一或多個屬性群組。</span><span class="sxs-lookup"><span data-stu-id="35577-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35577-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="35577-111">Return value</span></span>

<span data-ttu-id="35577-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35577-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35577-113">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="35577-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35577-114">備註</span><span class="sxs-lookup"><span data-stu-id="35577-114">Remarks</span></span>

<span data-ttu-id="35577-115">屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。</span><span class="sxs-lookup"><span data-stu-id="35577-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="35577-116">此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (AttribId) 繪製指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="35577-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="35577-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="35577-117">Requirements</span></span>



| <span data-ttu-id="35577-118">需求</span><span class="sxs-lookup"><span data-stu-id="35577-118">Requirement</span></span> | <span data-ttu-id="35577-119">值</span><span class="sxs-lookup"><span data-stu-id="35577-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35577-120">標頭</span><span class="sxs-lookup"><span data-stu-id="35577-120">Header</span></span><br/>  | <dl> <span data-ttu-id="35577-121"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="35577-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="35577-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="35577-122">Library</span></span><br/> | <dl> <span data-ttu-id="35577-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35577-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35577-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35577-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35577-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="35577-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="35577-126">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="35577-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
