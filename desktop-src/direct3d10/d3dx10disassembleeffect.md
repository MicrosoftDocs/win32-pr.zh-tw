---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DDisassemble API。 此函式會將已編譯的效果反組解碼為包含元件指令和註冊指派的文字字串--已被取代。
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: 'D3DX10DisassembleEffect 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946170"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="91415-104">D3DX10DisassembleEffect 函式</span><span class="sxs-lookup"><span data-stu-id="91415-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="91415-105">我們建議您不要使用此舊版函式，而是使用 [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API。</span><span class="sxs-lookup"><span data-stu-id="91415-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="91415-106">此函式會將已編譯的效果反組解碼為包含元件指令和註冊指派的文字字串--已被取代。</span><span class="sxs-lookup"><span data-stu-id="91415-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="91415-107">相反地，請使用 [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect)。</span><span class="sxs-lookup"><span data-stu-id="91415-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="91415-108">語法</span><span class="sxs-lookup"><span data-stu-id="91415-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="91415-109">參數</span><span class="sxs-lookup"><span data-stu-id="91415-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91415-110">*pEffect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91415-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91415-111">類型： **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="91415-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="91415-112">效果介面的指標 (查看 [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)) 。</span><span class="sxs-lookup"><span data-stu-id="91415-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="91415-113">*EnableColorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91415-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91415-114">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91415-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91415-115">在輸出中包含 HTML 標籤，以將結果色彩編碼。</span><span class="sxs-lookup"><span data-stu-id="91415-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="91415-116">*ppDisassembly* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="91415-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91415-117">類型： **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="91415-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="91415-118">緩衝區的位址 (查看包含拆解效果的 [**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。</span><span class="sxs-lookup"><span data-stu-id="91415-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91415-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="91415-119">Return value</span></span>

<span data-ttu-id="91415-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91415-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91415-121">傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="91415-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91415-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="91415-122">Requirements</span></span>



| <span data-ttu-id="91415-123">需求</span><span class="sxs-lookup"><span data-stu-id="91415-123">Requirement</span></span> | <span data-ttu-id="91415-124">值</span><span class="sxs-lookup"><span data-stu-id="91415-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91415-125">標頭</span><span class="sxs-lookup"><span data-stu-id="91415-125">Header</span></span><br/> | <dl> <span data-ttu-id="91415-126"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="91415-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91415-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91415-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91415-128">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="91415-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
