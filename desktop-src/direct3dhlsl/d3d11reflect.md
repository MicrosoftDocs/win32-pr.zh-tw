---
title: D3D11Reflect 函式
description: 取得反映介面的指標。
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect 函式 HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116281"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="d2beb-104">D3D11Reflect 函式</span><span class="sxs-lookup"><span data-stu-id="d2beb-104">D3D11Reflect function</span></span>

<span data-ttu-id="d2beb-105">取得反映介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d2beb-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2beb-106">語法</span><span class="sxs-lookup"><span data-stu-id="d2beb-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="d2beb-107">參數</span><span class="sxs-lookup"><span data-stu-id="d2beb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2beb-108">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2beb-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2beb-109">類型： **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2beb-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d2beb-110">作為已編譯 HLSL 程式碼之來源資料的指標。</span><span class="sxs-lookup"><span data-stu-id="d2beb-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="d2beb-111">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2beb-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2beb-112">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2beb-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d2beb-113">*PSrcData* 的長度。</span><span class="sxs-lookup"><span data-stu-id="d2beb-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="d2beb-114">*ppReflector* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d2beb-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2beb-115">類型： **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="d2beb-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="d2beb-116">[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="d2beb-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2beb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2beb-117">Return value</span></span>

<span data-ttu-id="d2beb-118">類型： **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d2beb-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d2beb-119">傳回 [Direct3D 11 傳回碼](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)主題中所述的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d2beb-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="d2beb-120">備註</span><span class="sxs-lookup"><span data-stu-id="d2beb-120">Remarks</span></span>

<span data-ttu-id="d2beb-121">內嵌 **D3D11Reflect** 編譯器函數是 [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) 編譯器函式的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="d2beb-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="d2beb-122">**D3D11Reflect** 只能從著色器取出 [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) 介面。</span><span class="sxs-lookup"><span data-stu-id="d2beb-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="d2beb-123">**D3DReflect** 可以取出 **ID3D11ShaderReflection** 介面或 direct3d 10 或 direct3d 10.1 反映介面，例如 [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection)。</span><span class="sxs-lookup"><span data-stu-id="d2beb-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="d2beb-124">著色器程式碼包含可使用反映 Api 檢查的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d2beb-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="d2beb-125">下列程式碼示範如何從著色器取出 [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) 介面。</span><span class="sxs-lookup"><span data-stu-id="d2beb-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="d2beb-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2beb-126">Requirements</span></span>



| <span data-ttu-id="d2beb-127">需求</span><span class="sxs-lookup"><span data-stu-id="d2beb-127">Requirement</span></span> | <span data-ttu-id="d2beb-128">值</span><span class="sxs-lookup"><span data-stu-id="d2beb-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2beb-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d2beb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d2beb-130"><dt>D3DCompiler. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="d2beb-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="d2beb-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2beb-131">Library</span></span><br/> | <dl> <span data-ttu-id="d2beb-132"><dt>D3dcompiler \_ 47 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2beb-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2beb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d2beb-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2beb-134"><dt>D3dcompiler \_47.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2beb-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2beb-135">請參閱</span><span class="sxs-lookup"><span data-stu-id="d2beb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2beb-136">函式</span><span class="sxs-lookup"><span data-stu-id="d2beb-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

