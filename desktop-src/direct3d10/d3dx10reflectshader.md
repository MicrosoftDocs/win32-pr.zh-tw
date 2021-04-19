---
description: 此函式會建立著色器反映物件，以抓取已編譯著色器的相關資訊--不存在。 請改用 D3DReflect 或 D3D11Reflect。
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: 'D3DX10ReflectShader 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000599"
---
# <a name="d3dx10reflectshader-function"></a><span data-ttu-id="90e76-104">D3DX10ReflectShader 函式</span><span class="sxs-lookup"><span data-stu-id="90e76-104">D3DX10ReflectShader function</span></span>

<span data-ttu-id="90e76-105">此函式會建立著色器反映物件，以抓取已編譯著色器的相關資訊--不存在。</span><span class="sxs-lookup"><span data-stu-id="90e76-105">This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- no longer exists.</span></span> <span data-ttu-id="90e76-106">請改用 [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) 或 [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md)。</span><span class="sxs-lookup"><span data-stu-id="90e76-106">Instead, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) or [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="90e76-107">語法</span><span class="sxs-lookup"><span data-stu-id="90e76-107">Syntax</span></span>


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a><span data-ttu-id="90e76-108">參數</span><span class="sxs-lookup"><span data-stu-id="90e76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e76-109">*pShaderBytecode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90e76-109">*pShaderBytecode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e76-110">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="90e76-110">Type: **const void\***</span></span>

<span data-ttu-id="90e76-111">已編譯之著色器的指標。</span><span class="sxs-lookup"><span data-stu-id="90e76-111">A pointer to the compiled shader.</span></span> <span data-ttu-id="90e76-112">若要取得此指標，請參閱 [取得已編譯著色器的指標](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)。</span><span class="sxs-lookup"><span data-stu-id="90e76-112">To get this pointer see [Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e76-113">*BytecodeLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90e76-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e76-114">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90e76-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90e76-115">PShaderBytecode 的長度。</span><span class="sxs-lookup"><span data-stu-id="90e76-115">Length of pShaderBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="90e76-116">*ppReflector* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="90e76-116">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90e76-117">類型： **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span><span class="sxs-lookup"><span data-stu-id="90e76-117">Type: **[**ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span></span>

<span data-ttu-id="90e76-118">著色器反映介面的位址 (查看 [**ID3D10ShaderReflection1 介面**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)。 ) </span><span class="sxs-lookup"><span data-stu-id="90e76-118">Address of a shader reflection interface (see [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90e76-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="90e76-119">Return value</span></span>

<span data-ttu-id="90e76-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90e76-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90e76-121">傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="90e76-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90e76-122">備註</span><span class="sxs-lookup"><span data-stu-id="90e76-122">Remarks</span></span>

<span data-ttu-id="90e76-123">以下是建立著色器反映物件的範例。</span><span class="sxs-lookup"><span data-stu-id="90e76-123">Here is an example of creating a shader-reflection object.</span></span> <span data-ttu-id="90e76-124">此範例假設您開始使用編譯的著色器 (顯示為</span><span class="sxs-lookup"><span data-stu-id="90e76-124">The example assumes you start with a compiled shader (shown as</span></span>


```
pVSBuf
```



<span data-ttu-id="90e76-125">您可以在 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)) 中看到。</span><span class="sxs-lookup"><span data-stu-id="90e76-125">which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a><span data-ttu-id="90e76-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="90e76-126">Requirements</span></span>



| <span data-ttu-id="90e76-127">需求</span><span class="sxs-lookup"><span data-stu-id="90e76-127">Requirement</span></span> | <span data-ttu-id="90e76-128">值</span><span class="sxs-lookup"><span data-stu-id="90e76-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90e76-129">標頭</span><span class="sxs-lookup"><span data-stu-id="90e76-129">Header</span></span><br/> | <dl> <span data-ttu-id="90e76-130"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="90e76-130"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e76-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90e76-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e76-132">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="90e76-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
