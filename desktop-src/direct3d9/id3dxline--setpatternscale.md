---
description: 沿著線條方向伸展 stipple 模式。
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine：： SetPatternScale 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196455"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="741ef-103">ID3DXLine：： SetPatternScale 方法</span><span class="sxs-lookup"><span data-stu-id="741ef-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="741ef-104">沿著線條方向伸展 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="741ef-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="741ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="741ef-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="741ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="741ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741ef-107">*fPatternScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="741ef-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741ef-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="741ef-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="741ef-109">Stipple 模式縮放比例值。</span><span class="sxs-lookup"><span data-stu-id="741ef-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="741ef-110">1.0 f 是預設值，不代表縮放比例。</span><span class="sxs-lookup"><span data-stu-id="741ef-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="741ef-111">小於 1.0 f 的值會壓縮模式，而大於1.0 的值會拉長模式。</span><span class="sxs-lookup"><span data-stu-id="741ef-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741ef-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="741ef-112">Return value</span></span>

<span data-ttu-id="741ef-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="741ef-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="741ef-114">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="741ef-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="741ef-115">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="741ef-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="741ef-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="741ef-116">Requirements</span></span>



| <span data-ttu-id="741ef-117">需求</span><span class="sxs-lookup"><span data-stu-id="741ef-117">Requirement</span></span> | <span data-ttu-id="741ef-118">值</span><span class="sxs-lookup"><span data-stu-id="741ef-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="741ef-119">標頭</span><span class="sxs-lookup"><span data-stu-id="741ef-119">Header</span></span><br/>  | <dl> <span data-ttu-id="741ef-120"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="741ef-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="741ef-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="741ef-121">Library</span></span><br/> | <dl> <span data-ttu-id="741ef-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="741ef-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="741ef-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="741ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741ef-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="741ef-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
