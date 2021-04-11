---
description: 判斷技術是否使用參數。
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'ID3DXEffect：： IsParameterUsed 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116185"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="fafbb-103">ID3DXEffect：： IsParameterUsed 方法</span><span class="sxs-lookup"><span data-stu-id="fafbb-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="fafbb-104">判斷技術是否使用參數。</span><span class="sxs-lookup"><span data-stu-id="fafbb-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafbb-105">語法</span><span class="sxs-lookup"><span data-stu-id="fafbb-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="fafbb-106">參數</span><span class="sxs-lookup"><span data-stu-id="fafbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafbb-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fafbb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fafbb-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fafbb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fafbb-109">參數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fafbb-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="fafbb-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="fafbb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fafbb-111">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fafbb-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fafbb-112">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fafbb-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fafbb-113">技術的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fafbb-113">Unique identifier for the technique.</span></span> <span data-ttu-id="fafbb-114">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="fafbb-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fafbb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fafbb-115">Return value</span></span>

<span data-ttu-id="fafbb-116">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fafbb-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fafbb-117">如果正在使用參數，則傳回 **TRUE** ，如果未使用參數，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fafbb-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fafbb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fafbb-118">Requirements</span></span>



| <span data-ttu-id="fafbb-119">需求</span><span class="sxs-lookup"><span data-stu-id="fafbb-119">Requirement</span></span> | <span data-ttu-id="fafbb-120">值</span><span class="sxs-lookup"><span data-stu-id="fafbb-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fafbb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fafbb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fafbb-122"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="fafbb-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fafbb-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="fafbb-123">Library</span></span><br/> | <dl> <span data-ttu-id="fafbb-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fafbb-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fafbb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fafbb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafbb-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="fafbb-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
