---
description: 取得著色器中所參考的取樣器名稱。
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: 'D3DXGetShaderSamplers 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986094"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="652e5-103">D3DXGetShaderSamplers 函式</span><span class="sxs-lookup"><span data-stu-id="652e5-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="652e5-104">取得著色器中所參考的取樣器名稱。</span><span class="sxs-lookup"><span data-stu-id="652e5-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="652e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="652e5-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="652e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="652e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="652e5-107">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="652e5-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652e5-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="652e5-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="652e5-109">著色器函式 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="652e5-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="652e5-110">*pSamplers* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="652e5-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="652e5-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="652e5-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="652e5-112">LPCSTRs 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="652e5-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="652e5-113">函式會使用 *pFunction* 中所包含之取樣器名稱的指標來填滿此陣列。</span><span class="sxs-lookup"><span data-stu-id="652e5-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="652e5-114">陣列大小上限是 vs \_ 3 \_ 0 和 ps \_ 3 \_ 0) 的取樣器暫存器數目上限 (16。</span><span class="sxs-lookup"><span data-stu-id="652e5-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="652e5-115">若要尋找使用的取樣器數目，請在使用 pSamplers = **Null** 呼叫 **D3DXGetShaderSamplers** 之後，檢查 *pCount* 。</span><span class="sxs-lookup"><span data-stu-id="652e5-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="652e5-116">*pCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="652e5-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="652e5-117">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="652e5-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="652e5-118">傳回著色器所參考的取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="652e5-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="652e5-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="652e5-119">Return value</span></span>

<span data-ttu-id="652e5-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="652e5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="652e5-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="652e5-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="652e5-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="652e5-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="652e5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="652e5-123">Requirements</span></span>



| <span data-ttu-id="652e5-124">需求</span><span class="sxs-lookup"><span data-stu-id="652e5-124">Requirement</span></span> | <span data-ttu-id="652e5-125">值</span><span class="sxs-lookup"><span data-stu-id="652e5-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="652e5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="652e5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="652e5-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="652e5-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="652e5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="652e5-128">Library</span></span><br/> | <dl> <span data-ttu-id="652e5-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="652e5-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="652e5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="652e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652e5-131">著色器函式</span><span class="sxs-lookup"><span data-stu-id="652e5-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
