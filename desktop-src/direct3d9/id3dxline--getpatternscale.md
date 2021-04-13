---
description: 取得 stipple 模式比例值。
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine：： GetPatternScale 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386526"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="2793b-103">ID3DXLine：： GetPatternScale 方法</span><span class="sxs-lookup"><span data-stu-id="2793b-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="2793b-104">取得 stipple 模式比例值。</span><span class="sxs-lookup"><span data-stu-id="2793b-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2793b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2793b-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="2793b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2793b-106">Parameters</span></span>

<span data-ttu-id="2793b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2793b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2793b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2793b-108">Return value</span></span>

<span data-ttu-id="2793b-109">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2793b-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2793b-110">傳回用來調整 stipple 模式的值。</span><span class="sxs-lookup"><span data-stu-id="2793b-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="2793b-111">1.0 f 是預設值，不代表縮放比例。</span><span class="sxs-lookup"><span data-stu-id="2793b-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="2793b-112">小於 1.0 f 的值會壓縮模式，而大於1.0 的值會拉長模式。</span><span class="sxs-lookup"><span data-stu-id="2793b-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="2793b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2793b-113">Requirements</span></span>



| <span data-ttu-id="2793b-114">需求</span><span class="sxs-lookup"><span data-stu-id="2793b-114">Requirement</span></span> | <span data-ttu-id="2793b-115">值</span><span class="sxs-lookup"><span data-stu-id="2793b-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2793b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="2793b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2793b-117"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="2793b-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2793b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="2793b-118">Library</span></span><br/> | <dl> <span data-ttu-id="2793b-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2793b-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2793b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2793b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2793b-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="2793b-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="2793b-122">**ID3DXLine::SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="2793b-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
