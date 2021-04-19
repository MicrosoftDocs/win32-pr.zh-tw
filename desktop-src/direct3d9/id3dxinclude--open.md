---
description: 使用者執行的方法，用來開啟和讀取著色器包含檔案的內容 \# 。
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude：： Open 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992351"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="4735d-103">ID3DXInclude：： Open 方法</span><span class="sxs-lookup"><span data-stu-id="4735d-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="4735d-104">使用者執行的方法，用來開啟和讀取著色器包含檔案的內容 \# 。</span><span class="sxs-lookup"><span data-stu-id="4735d-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4735d-105">語法</span><span class="sxs-lookup"><span data-stu-id="4735d-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="4735d-106">參數</span><span class="sxs-lookup"><span data-stu-id="4735d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4735d-107">*IncludeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4735d-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4735d-108">類型： **[ **D3DXINCLUDE \_ 類型**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="4735d-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="4735d-109">Include 檔案的位置 \# 。</span><span class="sxs-lookup"><span data-stu-id="4735d-109">The location of the \#include file.</span></span> <span data-ttu-id="4735d-110">請參閱 [**D3DXINCLUDE \_ 類型**](./d3dxinclude-type.md)。</span><span class="sxs-lookup"><span data-stu-id="4735d-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="4735d-111">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4735d-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4735d-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4735d-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4735d-113">Include 檔案的名稱 \# 。</span><span class="sxs-lookup"><span data-stu-id="4735d-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="4735d-114">*pParentData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4735d-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4735d-115">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4735d-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4735d-116">包含 include 檔之容器的指標 \# 。</span><span class="sxs-lookup"><span data-stu-id="4735d-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="4735d-117">編譯器可能會在 *pParentData* 中傳遞 Null。</span><span class="sxs-lookup"><span data-stu-id="4735d-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="4735d-118">如需詳細資訊，請參閱 [編譯效果 (Direct3D 11) ](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md)中的「搜尋 Include 檔」一節。</span><span class="sxs-lookup"><span data-stu-id="4735d-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="4735d-119">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4735d-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4735d-120">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4735d-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4735d-121">傳回之緩衝區的指標，其中包含 include 指示詞。</span><span class="sxs-lookup"><span data-stu-id="4735d-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="4735d-122">這個指標會維持有效，直到呼叫 [**ID3DXInclude：： Close**](id3dxinclude--close.md) 為止。</span><span class="sxs-lookup"><span data-stu-id="4735d-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="4735d-123">*pBytes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4735d-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4735d-124">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4735d-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4735d-125">PpData 中傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4735d-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4735d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="4735d-126">Return value</span></span>

<span data-ttu-id="4735d-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4735d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4735d-128">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4735d-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="4735d-129">如果回呼在讀取 include 檔案時失敗 \# ，則造成呼叫回呼的 API 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="4735d-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="4735d-130">這是下列項目之一：</span><span class="sxs-lookup"><span data-stu-id="4735d-130">This is one of the following:</span></span>

-   <span data-ttu-id="4735d-131">HLSL 著色器將會失敗其中一個 D3DXCompileShader \* \* \* 函數。</span><span class="sxs-lookup"><span data-stu-id="4735d-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="4735d-132">元件著色器將會使其中一個 D3DXAssembleShader 函式失敗 \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="4735d-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="4735d-133">此效果將會使其中一個 D3DXCreateEffect \* \* \* 或 D3DXCreateEffectCompiler \* \* \* 函數失敗。</span><span class="sxs-lookup"><span data-stu-id="4735d-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4735d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4735d-134">Requirements</span></span>



| <span data-ttu-id="4735d-135">需求</span><span class="sxs-lookup"><span data-stu-id="4735d-135">Requirement</span></span> | <span data-ttu-id="4735d-136">值</span><span class="sxs-lookup"><span data-stu-id="4735d-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4735d-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4735d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4735d-138"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="4735d-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4735d-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="4735d-139">Library</span></span><br/> | <dl> <span data-ttu-id="4735d-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4735d-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4735d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4735d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4735d-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="4735d-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="4735d-143">**ID3DXInclude：： Close**</span><span class="sxs-lookup"><span data-stu-id="4735d-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
