---
description: 藉由查詢名稱來取得最上層參數或結構成員參數的控制碼。
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'ID3DXBaseEffect：： GetParameterByName 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946250"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a><span data-ttu-id="13170-103">ID3DXBaseEffect：： GetParameterByName 方法</span><span class="sxs-lookup"><span data-stu-id="13170-103">ID3DXBaseEffect::GetParameterByName method</span></span>

<span data-ttu-id="13170-104">藉由查詢名稱來取得最上層參數或結構成員參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13170-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="13170-105">語法</span><span class="sxs-lookup"><span data-stu-id="13170-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="13170-106">參數</span><span class="sxs-lookup"><span data-stu-id="13170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13170-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13170-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13170-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="13170-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="13170-109">參數的控制碼，或最上層參數的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="13170-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="13170-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="13170-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="13170-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13170-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13170-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13170-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13170-113">包含參數名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="13170-113">String containing the parameter name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13170-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="13170-114">Return value</span></span>

<span data-ttu-id="13170-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="13170-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="13170-116">傳回指定之參數的控制碼，如果索引無效，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="13170-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="13170-117">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="13170-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13170-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="13170-118">Requirements</span></span>



| <span data-ttu-id="13170-119">需求</span><span class="sxs-lookup"><span data-stu-id="13170-119">Requirement</span></span> | <span data-ttu-id="13170-120">值</span><span class="sxs-lookup"><span data-stu-id="13170-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13170-121">標頭</span><span class="sxs-lookup"><span data-stu-id="13170-121">Header</span></span><br/>  | <dl> <span data-ttu-id="13170-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="13170-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="13170-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="13170-123">Library</span></span><br/> | <dl> <span data-ttu-id="13170-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13170-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="13170-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13170-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13170-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="13170-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
