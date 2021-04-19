---
description: 傳回取樣器索引。
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'ID3DXConstantTable：： GetSamplerIndex 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998208"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a><span data-ttu-id="6674a-103">ID3DXConstantTable：： GetSamplerIndex 方法</span><span class="sxs-lookup"><span data-stu-id="6674a-103">ID3DXConstantTable::GetSamplerIndex method</span></span>

<span data-ttu-id="6674a-104">傳回取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="6674a-104">Returns the sampler index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6674a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6674a-105">Syntax</span></span>


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a><span data-ttu-id="6674a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6674a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6674a-107">*hConstant* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6674a-107">*hConstant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6674a-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6674a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6674a-109">取樣器處理。</span><span class="sxs-lookup"><span data-stu-id="6674a-109">The sampler handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6674a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6674a-110">Return value</span></span>

<span data-ttu-id="6674a-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6674a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6674a-112">從常數資料表傳回取樣器索引編號。</span><span class="sxs-lookup"><span data-stu-id="6674a-112">Returns the sampler index number from the constant table.</span></span>

## <a name="requirements"></a><span data-ttu-id="6674a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6674a-113">Requirements</span></span>



| <span data-ttu-id="6674a-114">需求</span><span class="sxs-lookup"><span data-stu-id="6674a-114">Requirement</span></span> | <span data-ttu-id="6674a-115">值</span><span class="sxs-lookup"><span data-stu-id="6674a-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6674a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="6674a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6674a-117"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="6674a-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6674a-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="6674a-118">Library</span></span><br/> | <dl> <span data-ttu-id="6674a-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6674a-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6674a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6674a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6674a-121">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6674a-121">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
