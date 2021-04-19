---
description: 建立新的網格，並將其填入先前載入之網格的資料。
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh：： CloneMesh 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991971"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="561a9-103">ID3DX10Mesh：： CloneMesh 方法</span><span class="sxs-lookup"><span data-stu-id="561a9-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="561a9-104">建立新的網格，並將其填入先前載入之網格的資料。</span><span class="sxs-lookup"><span data-stu-id="561a9-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="561a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="561a9-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="561a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="561a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="561a9-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="561a9-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="561a9-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="561a9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="561a9-109">要套用至新網格的建立旗標。</span><span class="sxs-lookup"><span data-stu-id="561a9-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="561a9-110">請參閱 [**D3DX10 \_ 網格**](d3dx10-mesh.md)。</span><span class="sxs-lookup"><span data-stu-id="561a9-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="561a9-111">*pPosSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="561a9-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="561a9-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="561a9-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="561a9-113">位置資料的語義名稱。</span><span class="sxs-lookup"><span data-stu-id="561a9-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="561a9-114">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="561a9-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="561a9-115">Type： **Const [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="561a9-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="561a9-116">D3D10 \_ 輸入 \_ 元素 \_ DESC 結構的陣列，描述傳回之網格的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="561a9-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="561a9-117">請參閱 [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)。</span><span class="sxs-lookup"><span data-stu-id="561a9-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="561a9-118">*DeclCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="561a9-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="561a9-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="561a9-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="561a9-120">PDesc 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="561a9-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="561a9-121">*ppCloneMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="561a9-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="561a9-122">類型： **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="561a9-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="561a9-123">新的網格。</span><span class="sxs-lookup"><span data-stu-id="561a9-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="561a9-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="561a9-124">Return value</span></span>

<span data-ttu-id="561a9-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="561a9-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="561a9-126">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="561a9-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="561a9-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="561a9-127">Requirements</span></span>



| <span data-ttu-id="561a9-128">需求</span><span class="sxs-lookup"><span data-stu-id="561a9-128">Requirement</span></span> | <span data-ttu-id="561a9-129">值</span><span class="sxs-lookup"><span data-stu-id="561a9-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="561a9-130">標頭</span><span class="sxs-lookup"><span data-stu-id="561a9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="561a9-131"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="561a9-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="561a9-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="561a9-132">Library</span></span><br/> | <dl> <span data-ttu-id="561a9-133"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="561a9-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="561a9-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="561a9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="561a9-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="561a9-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="561a9-136">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="561a9-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
