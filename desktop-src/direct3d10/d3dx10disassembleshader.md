---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DDisassemble API。 這個函式--將已編譯的著色器反組解碼為包含元件指令和註冊指派的文字字串--不存在。
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: 'D3DX10DisassembleShader 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981806"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="a21ee-104">D3DX10DisassembleShader 函式</span><span class="sxs-lookup"><span data-stu-id="a21ee-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="a21ee-105">我們建議您不要使用此舊版函式，而是使用 [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API。</span><span class="sxs-lookup"><span data-stu-id="a21ee-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="a21ee-106">這個函式--將已編譯的著色器反組解碼為包含元件指令和註冊指派的文字字串--不存在。</span><span class="sxs-lookup"><span data-stu-id="a21ee-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="a21ee-107">相反地，請使用 [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect)。</span><span class="sxs-lookup"><span data-stu-id="a21ee-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="a21ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="a21ee-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="a21ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="a21ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21ee-110">*pShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a21ee-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a21ee-111">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="a21ee-111">Type: **const void\***</span></span>

<span data-ttu-id="a21ee-112">[**已編譯之著色器**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)的指標。</span><span class="sxs-lookup"><span data-stu-id="a21ee-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="a21ee-113">*BytecodeLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a21ee-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a21ee-114">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a21ee-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a21ee-115">PShader 的大小。</span><span class="sxs-lookup"><span data-stu-id="a21ee-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="a21ee-116">*EnableColorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a21ee-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a21ee-117">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a21ee-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a21ee-118">在輸出中包含 HTML 標籤，以將結果色彩編碼。</span><span class="sxs-lookup"><span data-stu-id="a21ee-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="a21ee-119">*pComments* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a21ee-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a21ee-120">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a21ee-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a21ee-121">著色器頂端的批註字串，可識別著色器的常數和變數。</span><span class="sxs-lookup"><span data-stu-id="a21ee-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="a21ee-122">*ppDisassembly* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a21ee-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a21ee-123">類型： **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a21ee-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a21ee-124">緩衝區的位址 (參閱 [**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) ，其中包含已拆解的著色器。</span><span class="sxs-lookup"><span data-stu-id="a21ee-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21ee-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="a21ee-125">Return value</span></span>

<span data-ttu-id="a21ee-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a21ee-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a21ee-127">傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="a21ee-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a21ee-128">備註</span><span class="sxs-lookup"><span data-stu-id="a21ee-128">Remarks</span></span>

<span data-ttu-id="a21ee-129">這項傳回的文字包含一個標頭，其中包含用來產生此物件的 HLSL 編譯器版本、描述著色器所使用之常數緩衝區記憶體配置的批註、輸入和輸出簽章，以及資源系結點。</span><span class="sxs-lookup"><span data-stu-id="a21ee-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="a21ee-130">以下是將已編譯的著色器分解的範例。</span><span class="sxs-lookup"><span data-stu-id="a21ee-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="a21ee-131">此範例假設您從已編譯的著色器開始 (顯示為 *pVSBuf* ，您可以在 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)) 中看到。</span><span class="sxs-lookup"><span data-stu-id="a21ee-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="a21ee-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="a21ee-132">Requirements</span></span>



| <span data-ttu-id="a21ee-133">需求</span><span class="sxs-lookup"><span data-stu-id="a21ee-133">Requirement</span></span> | <span data-ttu-id="a21ee-134">值</span><span class="sxs-lookup"><span data-stu-id="a21ee-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a21ee-135">標頭</span><span class="sxs-lookup"><span data-stu-id="a21ee-135">Header</span></span><br/> | <dl> <span data-ttu-id="a21ee-136"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="a21ee-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21ee-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a21ee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21ee-138">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="a21ee-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
