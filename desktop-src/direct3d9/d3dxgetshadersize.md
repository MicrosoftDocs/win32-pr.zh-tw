---
description: 傳回著色器位元組程式碼的大小（以位元組為單位）。
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: 'D3DXGetShaderSize 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986738"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="56a51-103">D3DXGetShaderSize 函式</span><span class="sxs-lookup"><span data-stu-id="56a51-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="56a51-104">傳回著色器位元組程式碼的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="56a51-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a51-105">語法</span><span class="sxs-lookup"><span data-stu-id="56a51-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="56a51-106">參數</span><span class="sxs-lookup"><span data-stu-id="56a51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a51-107">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56a51-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a51-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="56a51-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56a51-109">函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="56a51-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a51-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="56a51-110">Return value</span></span>

<span data-ttu-id="56a51-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a51-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56a51-112">傳回著色器位元組程式碼的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="56a51-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a51-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a51-113">Requirements</span></span>



| <span data-ttu-id="56a51-114">需求</span><span class="sxs-lookup"><span data-stu-id="56a51-114">Requirement</span></span> | <span data-ttu-id="56a51-115">值</span><span class="sxs-lookup"><span data-stu-id="56a51-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56a51-116">標頭</span><span class="sxs-lookup"><span data-stu-id="56a51-116">Header</span></span><br/>  | <dl> <span data-ttu-id="56a51-117"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="56a51-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="56a51-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="56a51-118">Library</span></span><br/> | <dl> <span data-ttu-id="56a51-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="56a51-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="56a51-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56a51-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a51-121">著色器函式</span><span class="sxs-lookup"><span data-stu-id="56a51-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
