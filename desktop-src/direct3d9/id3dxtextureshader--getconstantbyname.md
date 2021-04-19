---
description: 藉由查詢名稱來取得常數。
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'ID3DXTextureShader：： GetConstantByName 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a285da2fa3179f91d34eda8d9ce1f622c86df15b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992739"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="fd472-103">ID3DXTextureShader：： GetConstantByName 方法</span><span class="sxs-lookup"><span data-stu-id="fd472-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="fd472-104">藉由查詢名稱來取得常數。</span><span class="sxs-lookup"><span data-stu-id="fd472-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd472-105">語法</span><span class="sxs-lookup"><span data-stu-id="fd472-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="fd472-106">參數</span><span class="sxs-lookup"><span data-stu-id="fd472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd472-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd472-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd472-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fd472-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fd472-109">父資料結構的 [控制碼](handles.md) 。</span><span class="sxs-lookup"><span data-stu-id="fd472-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="fd472-110">如果常數是最上層參數 (沒有任何父資料結構) ，請使用 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fd472-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fd472-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd472-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd472-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd472-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd472-113">字串，包含常數的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd472-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd472-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd472-114">Return value</span></span>

<span data-ttu-id="fd472-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fd472-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fd472-116">傳回常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd472-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd472-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd472-117">Requirements</span></span>



| <span data-ttu-id="fd472-118">需求</span><span class="sxs-lookup"><span data-stu-id="fd472-118">Requirement</span></span> | <span data-ttu-id="fd472-119">值</span><span class="sxs-lookup"><span data-stu-id="fd472-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd472-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fd472-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fd472-121"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd472-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fd472-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd472-122">Library</span></span><br/> | <dl> <span data-ttu-id="fd472-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd472-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fd472-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd472-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd472-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="fd472-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
