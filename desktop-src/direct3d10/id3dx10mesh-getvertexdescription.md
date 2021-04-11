---
description: 存取傳遞至 D3DX10CreateMesh 的頂點描述。 頂點描述描述網格頂點緩衝區的版面配置。
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'ID3DX10Mesh：： GetVertexDescription 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946109"
---
# <a name="id3dx10meshgetvertexdescription-method"></a><span data-ttu-id="f4f7c-104">ID3DX10Mesh：： GetVertexDescription 方法</span><span class="sxs-lookup"><span data-stu-id="f4f7c-104">ID3DX10Mesh::GetVertexDescription method</span></span>

<span data-ttu-id="f4f7c-105">存取傳遞至 [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)的頂點描述。</span><span class="sxs-lookup"><span data-stu-id="f4f7c-105">Access the vertex description passed into [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span></span> <span data-ttu-id="f4f7c-106">頂點描述描述網格頂點緩衝區的版面配置。</span><span class="sxs-lookup"><span data-stu-id="f4f7c-106">The vertex description describes the layout of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f7c-107">語法</span><span class="sxs-lookup"><span data-stu-id="f4f7c-107">Syntax</span></span>


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a><span data-ttu-id="f4f7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="f4f7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f7c-109">*ppDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f4f7c-109">*ppDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f7c-110">Type： **Const [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***</span><span class="sxs-lookup"><span data-stu-id="f4f7c-110">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\*\***</span></span>

<span data-ttu-id="f4f7c-111">描述網格頂點緩衝區配置的輸入元素陣列。</span><span class="sxs-lookup"><span data-stu-id="f4f7c-111">Array of input elements that describe the layout of the mesh's vertex buffers.</span></span> <span data-ttu-id="f4f7c-112">請參閱 [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)。</span><span class="sxs-lookup"><span data-stu-id="f4f7c-112">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="f4f7c-113">*pDeclCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4f7c-113">*pDeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f7c-114">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4f7c-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f4f7c-115">PpDesc 中輸入元素的數目。</span><span class="sxs-lookup"><span data-stu-id="f4f7c-115">The number of input elements in ppDesc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f7c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4f7c-116">Return value</span></span>

<span data-ttu-id="f4f7c-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4f7c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4f7c-118">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f4f7c-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f7c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4f7c-119">Requirements</span></span>



| <span data-ttu-id="f4f7c-120">需求</span><span class="sxs-lookup"><span data-stu-id="f4f7c-120">Requirement</span></span> | <span data-ttu-id="f4f7c-121">值</span><span class="sxs-lookup"><span data-stu-id="f4f7c-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f7c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f4f7c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f4f7c-123"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f7c-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4f7c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="f4f7c-124">Library</span></span><br/> | <dl> <span data-ttu-id="f4f7c-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4f7c-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f7c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4f7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f7c-127">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f4f7c-127">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f4f7c-128">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f4f7c-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
