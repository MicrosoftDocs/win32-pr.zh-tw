---
description: 取得所有著色器輸出元素的語法。
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: 'D3DXGetShaderOutputSemantics 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514593"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="77aeb-103">D3DXGetShaderOutputSemantics 函式</span><span class="sxs-lookup"><span data-stu-id="77aeb-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="77aeb-104">取得所有著色器輸出元素的語法。</span><span class="sxs-lookup"><span data-stu-id="77aeb-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="77aeb-105">語法</span><span class="sxs-lookup"><span data-stu-id="77aeb-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="77aeb-106">參數</span><span class="sxs-lookup"><span data-stu-id="77aeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77aeb-107">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77aeb-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77aeb-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="77aeb-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="77aeb-109">著色器函式 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="77aeb-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="77aeb-110">*pSemantics* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77aeb-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77aeb-111">類型： **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="77aeb-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="77aeb-112">[**D3DXSEMANTIC**](d3dxsemantic.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="77aeb-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="77aeb-113">此函式會使用著色器所參考之每個輸出專案的語義來填滿此陣列。</span><span class="sxs-lookup"><span data-stu-id="77aeb-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="77aeb-114">此陣列假設至少包含 MAXD3DDECLLENGTH 元素。</span><span class="sxs-lookup"><span data-stu-id="77aeb-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="77aeb-115">不過，使用 pSemantics = **Null** 呼叫 **D3DXGetShaderOutputSemantics** 會傳回 pCount 所需的元素數目。</span><span class="sxs-lookup"><span data-stu-id="77aeb-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="77aeb-116">*pCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77aeb-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77aeb-117">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="77aeb-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="77aeb-118">傳回 pSemantics 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="77aeb-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77aeb-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="77aeb-119">Return value</span></span>

<span data-ttu-id="77aeb-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77aeb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77aeb-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="77aeb-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="77aeb-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="77aeb-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="77aeb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="77aeb-123">Requirements</span></span>



| <span data-ttu-id="77aeb-124">需求</span><span class="sxs-lookup"><span data-stu-id="77aeb-124">Requirement</span></span> | <span data-ttu-id="77aeb-125">值</span><span class="sxs-lookup"><span data-stu-id="77aeb-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77aeb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="77aeb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="77aeb-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="77aeb-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="77aeb-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="77aeb-128">Library</span></span><br/> | <dl> <span data-ttu-id="77aeb-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="77aeb-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="77aeb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77aeb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77aeb-131">著色器函式</span><span class="sxs-lookup"><span data-stu-id="77aeb-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
