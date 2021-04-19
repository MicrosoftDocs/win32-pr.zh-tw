---
description: 取得著色器輸入的語法。 您可以使用這個方法來判斷輸入頂點格式。
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: 'D3DXGetShaderInputSemantics 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982010"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="d4988-104">D3DXGetShaderInputSemantics 函式</span><span class="sxs-lookup"><span data-stu-id="d4988-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="d4988-105">取得著色器輸入的語法。</span><span class="sxs-lookup"><span data-stu-id="d4988-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="d4988-106">您可以使用這個方法來判斷輸入頂點格式。</span><span class="sxs-lookup"><span data-stu-id="d4988-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4988-107">語法</span><span class="sxs-lookup"><span data-stu-id="d4988-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="d4988-108">參數</span><span class="sxs-lookup"><span data-stu-id="d4988-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4988-109">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4988-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4988-110">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4988-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d4988-111">著色器函式 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="d4988-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4988-112">*pSemantics* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4988-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4988-113">類型： **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4988-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="d4988-114">[**D3DXSEMANTIC**](d3dxsemantic.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d4988-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="d4988-115">此函式會使用著色器所參考的每個輸入專案的語義來填滿此陣列。</span><span class="sxs-lookup"><span data-stu-id="d4988-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="d4988-116">此陣列假設至少包含 MAXD3DDECLLENGTH 元素。</span><span class="sxs-lookup"><span data-stu-id="d4988-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="d4988-117">不過，使用 pSemantics = **Null** 呼叫 **D3DXGetShaderInputSemantics** 會傳回 pCount 所需的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d4988-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="d4988-118">*pCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d4988-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4988-119">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4988-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d4988-120">傳回 pSemantics 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d4988-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4988-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4988-121">Return value</span></span>

<span data-ttu-id="d4988-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4988-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4988-123">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d4988-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d4988-124">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="d4988-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4988-125">備註</span><span class="sxs-lookup"><span data-stu-id="d4988-125">Remarks</span></span>

<span data-ttu-id="d4988-126">使用 **D3DXGetShaderInputSemantics** 傳回著色器所需的輸入語義清單。</span><span class="sxs-lookup"><span data-stu-id="d4988-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="d4988-127">這是用來找出高階著色器語言 (HLSL) 著色器的輸入頂點格式的方式。</span><span class="sxs-lookup"><span data-stu-id="d4988-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="d4988-128">如果著色器有遺漏您頂點宣告的其他輸入，您可以建立具有值為0的額外頂點資料流程，其具有預設值的遺漏元件。</span><span class="sxs-lookup"><span data-stu-id="d4988-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="d4988-129">比方說，這項技術可以用來為未指定的模型提供預設頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="d4988-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4988-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4988-130">Requirements</span></span>



| <span data-ttu-id="d4988-131">需求</span><span class="sxs-lookup"><span data-stu-id="d4988-131">Requirement</span></span> | <span data-ttu-id="d4988-132">值</span><span class="sxs-lookup"><span data-stu-id="d4988-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4988-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d4988-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d4988-134"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4988-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d4988-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4988-135">Library</span></span><br/> | <dl> <span data-ttu-id="d4988-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4988-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d4988-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4988-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4988-138">著色器函式</span><span class="sxs-lookup"><span data-stu-id="d4988-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
