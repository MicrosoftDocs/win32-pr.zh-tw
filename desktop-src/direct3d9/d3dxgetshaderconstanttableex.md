---
description: D3DXGetShaderConstantTableEx 函式-取得內嵌在著色器中的著色器常數資料表。
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: 'D3DXGetShaderConstantTableEx 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114426"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="2c041-103">D3DXGetShaderConstantTableEx 函式</span><span class="sxs-lookup"><span data-stu-id="2c041-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="2c041-104">取得內嵌在著色器中的著色器常數資料表。</span><span class="sxs-lookup"><span data-stu-id="2c041-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c041-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c041-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="2c041-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c041-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c041-107">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c041-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c041-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c041-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2c041-109">函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="2c041-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="2c041-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2c041-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c041-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c041-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c041-112">使用 D3DXCONSTTABLE \_ LARGEADDRESSAWARE 旗標可存取最多 4 gb 的虛擬位址空間 (而不是預設的 2 gb) 。</span><span class="sxs-lookup"><span data-stu-id="2c041-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="2c041-113">如果您不需要額外的虛擬位址空間，請使用 [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)。</span><span class="sxs-lookup"><span data-stu-id="2c041-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="2c041-114">*ppConstantTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c041-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c041-115">類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c041-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="2c041-116">傳回常數資料表介面 (查看管理常數資料表的 [**ID3DXConstantTable**](id3dxconstanttable.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2c041-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c041-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c041-117">Return value</span></span>

<span data-ttu-id="2c041-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c041-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c041-119">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2c041-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c041-120">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2c041-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c041-121">備註</span><span class="sxs-lookup"><span data-stu-id="2c041-121">Remarks</span></span>

<span data-ttu-id="2c041-122">常數資料表是由 [**D3DXCompileShader**](d3dxcompileshader.md) 所產生，並內嵌在著色器主體中。</span><span class="sxs-lookup"><span data-stu-id="2c041-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c041-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c041-123">Requirements</span></span>



| <span data-ttu-id="2c041-124">需求</span><span class="sxs-lookup"><span data-stu-id="2c041-124">Requirement</span></span> | <span data-ttu-id="2c041-125">值</span><span class="sxs-lookup"><span data-stu-id="2c041-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c041-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2c041-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2c041-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c041-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2c041-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c041-128">Library</span></span><br/> | <dl> <span data-ttu-id="2c041-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c041-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2c041-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c041-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c041-131">著色器函式</span><span class="sxs-lookup"><span data-stu-id="2c041-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
