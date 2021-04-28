---
description: D3DXGetVertexShaderProfile 函式-傳回指定裝置所支援的最高高階著色器語言 (HLSL) 設定檔的名稱。
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: 'D3DXGetVertexShaderProfile 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70d6cdf79fdd91e819d54702682515aa3e4810b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114456"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="68ed4-103">D3DXGetVertexShaderProfile 函式</span><span class="sxs-lookup"><span data-stu-id="68ed4-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="68ed4-104">傳回指定裝置支援的最高階著色器語言 (HLSL) 設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="68ed4-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ed4-105">語法</span><span class="sxs-lookup"><span data-stu-id="68ed4-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="68ed4-106">參數</span><span class="sxs-lookup"><span data-stu-id="68ed4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68ed4-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68ed4-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68ed4-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="68ed4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="68ed4-109">裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="68ed4-109">Pointer to the device.</span></span> <span data-ttu-id="68ed4-110">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="68ed4-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68ed4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="68ed4-111">Return value</span></span>

<span data-ttu-id="68ed4-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68ed4-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68ed4-113">HLSL 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="68ed4-113">The HLSL profile name.</span></span>

<span data-ttu-id="68ed4-114">如果裝置不支援頂點著色器，則函數會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="68ed4-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68ed4-115">備註</span><span class="sxs-lookup"><span data-stu-id="68ed4-115">Remarks</span></span>

<span data-ttu-id="68ed4-116">著色器設定檔會指定要使用的元件著色器版本，以及編譯著色器時可供 HLSL 編譯器使用的功能。</span><span class="sxs-lookup"><span data-stu-id="68ed4-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="68ed4-117">下表列出支援的頂點著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="68ed4-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68ed4-118">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="68ed4-118">Shader Profile</span></span></th>
<th><span data-ttu-id="68ed4-119">Description</span><span class="sxs-lookup"><span data-stu-id="68ed4-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68ed4-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="68ed4-120">vs_1_1</span></span></td>
<td><span data-ttu-id="68ed4-121">編譯為 vs_1_1 版本。</span><span class="sxs-lookup"><span data-stu-id="68ed4-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ed4-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="68ed4-122">vs_2_0</span></span></td>
<td><span data-ttu-id="68ed4-123">編譯為 vs_2_0 版本。</span><span class="sxs-lookup"><span data-stu-id="68ed4-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68ed4-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="68ed4-124">vs_2_a</span></span></td>
<td><span data-ttu-id="68ed4-125">如同 vs_2_0 設定檔，具有下列可供編譯器使用的其他功能：</span><span class="sxs-lookup"><span data-stu-id="68ed4-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="68ed4-126"> (r # ) 大於或等於13的臨時暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="68ed4-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="68ed4-127">動態流程式控制制指令。</span><span class="sxs-lookup"><span data-stu-id="68ed4-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="68ed4-128">預測。</span><span class="sxs-lookup"><span data-stu-id="68ed4-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68ed4-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="68ed4-129">vs_3_0</span></span></td>
<td><span data-ttu-id="68ed4-130">編譯為 vs_3_0 版本。</span><span class="sxs-lookup"><span data-stu-id="68ed4-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="68ed4-131">如需著色器版本之間差異的詳細資訊，請參閱 [頂點著色器差異](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="68ed4-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68ed4-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="68ed4-132">Requirements</span></span>



| <span data-ttu-id="68ed4-133">需求</span><span class="sxs-lookup"><span data-stu-id="68ed4-133">Requirement</span></span> | <span data-ttu-id="68ed4-134">值</span><span class="sxs-lookup"><span data-stu-id="68ed4-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ed4-135">標頭</span><span class="sxs-lookup"><span data-stu-id="68ed4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="68ed4-136"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="68ed4-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="68ed4-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="68ed4-137">Library</span></span><br/> | <dl> <span data-ttu-id="68ed4-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68ed4-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="68ed4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68ed4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ed4-140">著色器函式</span><span class="sxs-lookup"><span data-stu-id="68ed4-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
