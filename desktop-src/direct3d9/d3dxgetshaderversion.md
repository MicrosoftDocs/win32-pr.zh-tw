---
description: 傳回已編譯著色器的著色器版本。
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: 'D3DXGetShaderVersion 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116221"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="c6178-103">D3DXGetShaderVersion 函式</span><span class="sxs-lookup"><span data-stu-id="c6178-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="c6178-104">傳回已編譯著色器的著色器版本。</span><span class="sxs-lookup"><span data-stu-id="c6178-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6178-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6178-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="c6178-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6178-107">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6178-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6178-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c6178-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c6178-109">函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="c6178-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6178-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6178-110">Return value</span></span>

<span data-ttu-id="c6178-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6178-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c6178-112">傳回指定著色器的著色器版本，如果著色器函式為 **Null**，則為零。</span><span class="sxs-lookup"><span data-stu-id="c6178-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6178-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6178-113">Requirements</span></span>



| <span data-ttu-id="c6178-114">需求</span><span class="sxs-lookup"><span data-stu-id="c6178-114">Requirement</span></span> | <span data-ttu-id="c6178-115">值</span><span class="sxs-lookup"><span data-stu-id="c6178-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6178-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c6178-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c6178-117"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6178-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c6178-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c6178-118">Library</span></span><br/> | <dl> <span data-ttu-id="c6178-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6178-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c6178-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6178-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6178-121">著色器函式</span><span class="sxs-lookup"><span data-stu-id="c6178-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
