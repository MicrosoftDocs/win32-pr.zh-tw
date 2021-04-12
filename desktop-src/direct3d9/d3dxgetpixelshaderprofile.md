---
description: 傳回指定裝置支援的最高階著色器語言 (HLSL) 設定檔的名稱。
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: 'D3DXGetPixelShaderProfile 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946096"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="bfc17-103">D3DXGetPixelShaderProfile 函式</span><span class="sxs-lookup"><span data-stu-id="bfc17-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="bfc17-104">傳回指定裝置支援的最高階著色器語言 (HLSL) 設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="bfc17-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc17-105">語法</span><span class="sxs-lookup"><span data-stu-id="bfc17-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="bfc17-106">參數</span><span class="sxs-lookup"><span data-stu-id="bfc17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc17-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfc17-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc17-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bfc17-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bfc17-109">裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="bfc17-109">Pointer to the device.</span></span> <span data-ttu-id="bfc17-110">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="bfc17-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc17-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfc17-111">Return value</span></span>

<span data-ttu-id="bfc17-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfc17-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bfc17-113">HLSL 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="bfc17-113">The HLSL profile name.</span></span>

<span data-ttu-id="bfc17-114">如果裝置不支援圖元著色器，則函數會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bfc17-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfc17-115">備註</span><span class="sxs-lookup"><span data-stu-id="bfc17-115">Remarks</span></span>

<span data-ttu-id="bfc17-116">著色器設定檔會指定要使用的元件著色器版本，以及編譯著色器時可供 HLSL 編譯器使用的功能。</span><span class="sxs-lookup"><span data-stu-id="bfc17-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="bfc17-117">下表列出支援的圖元著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="bfc17-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfc17-118">著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="bfc17-118">Shader Profile</span></span></th>
<th><span data-ttu-id="bfc17-119">Description</span><span class="sxs-lookup"><span data-stu-id="bfc17-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bfc17-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="bfc17-120">ps_1_1</span></span></td>
<td><span data-ttu-id="bfc17-121">編譯為 ps_1_1 版本。</span><span class="sxs-lookup"><span data-stu-id="bfc17-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc17-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="bfc17-122">ps_1_2</span></span></td>
<td><span data-ttu-id="bfc17-123">編譯為 ps_1_2 版本。</span><span class="sxs-lookup"><span data-stu-id="bfc17-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc17-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="bfc17-124">ps_1_3</span></span></td>
<td><span data-ttu-id="bfc17-125">編譯為 ps_1_3 版本。</span><span class="sxs-lookup"><span data-stu-id="bfc17-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc17-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="bfc17-126">ps_1_4</span></span></td>
<td><span data-ttu-id="bfc17-127">編譯為 ps_1_4 版本。</span><span class="sxs-lookup"><span data-stu-id="bfc17-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc17-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="bfc17-128">ps_2_0</span></span></td>
<td><span data-ttu-id="bfc17-129">編譯為 ps_2_0 版本。</span><span class="sxs-lookup"><span data-stu-id="bfc17-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc17-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="bfc17-130">ps_2_a</span></span></td>
<td><span data-ttu-id="bfc17-131">如同 ps_2_0 設定檔，具有下列可供編譯器使用的其他功能：</span><span class="sxs-lookup"><span data-stu-id="bfc17-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="bfc17-132"> (r # ) 大於或等於22的臨時暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="bfc17-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="bfc17-133">任意來源 swizzle。</span><span class="sxs-lookup"><span data-stu-id="bfc17-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="bfc17-134">漸層指示： dsx、dsy。</span><span class="sxs-lookup"><span data-stu-id="bfc17-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="bfc17-135">預測。</span><span class="sxs-lookup"><span data-stu-id="bfc17-135">Predication.</span></span></li>
<li><span data-ttu-id="bfc17-136">沒有相依材質讀取限制。</span><span class="sxs-lookup"><span data-stu-id="bfc17-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="bfc17-137">材質指令數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="bfc17-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfc17-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="bfc17-138">ps_2_b</span></span></td>
<td><span data-ttu-id="bfc17-139">如同 ps_2_0 設定檔，具有下列可供編譯器使用的其他功能：</span><span class="sxs-lookup"><span data-stu-id="bfc17-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="bfc17-140"> (r # ) 大於或等於32的臨時暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="bfc17-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="bfc17-141">材質指令數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="bfc17-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfc17-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="bfc17-142">ps_3_0</span></span></td>
<td><span data-ttu-id="bfc17-143">編譯為 ps_3_0 版本。</span><span class="sxs-lookup"><span data-stu-id="bfc17-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bfc17-144">如需著色器版本之間差異的詳細資訊，請參閱 [圖元著色器差異](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="bfc17-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc17-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfc17-145">Requirements</span></span>



| <span data-ttu-id="bfc17-146">需求</span><span class="sxs-lookup"><span data-stu-id="bfc17-146">Requirement</span></span> | <span data-ttu-id="bfc17-147">值</span><span class="sxs-lookup"><span data-stu-id="bfc17-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc17-148">標頭</span><span class="sxs-lookup"><span data-stu-id="bfc17-148">Header</span></span><br/>  | <dl> <span data-ttu-id="bfc17-149"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc17-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bfc17-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="bfc17-150">Library</span></span><br/> | <dl> <span data-ttu-id="bfc17-151"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfc17-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bfc17-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfc17-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc17-153">著色器函式</span><span class="sxs-lookup"><span data-stu-id="bfc17-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
