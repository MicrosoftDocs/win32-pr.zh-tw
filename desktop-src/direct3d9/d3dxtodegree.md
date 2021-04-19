---
description: 將弧度轉換為度數。
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: 'D3DXToDegree (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToDegree
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: ad77ea661f4d67318566079aa7c1072fe0f86c91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997618"
---
# <a name="d3dxtodegree"></a><span data-ttu-id="81d88-103">D3DXToDegree</span><span class="sxs-lookup"><span data-stu-id="81d88-103">D3DXToDegree</span></span>

<span data-ttu-id="81d88-104">將弧度轉換為度數。</span><span class="sxs-lookup"><span data-stu-id="81d88-104">Converts radians into degrees.</span></span>

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a><span data-ttu-id="81d88-105">參數</span><span class="sxs-lookup"><span data-stu-id="81d88-105">Parameters</span></span>



| <span data-ttu-id="81d88-106">參數</span><span class="sxs-lookup"><span data-stu-id="81d88-106">Parameter</span></span>                                                           | <span data-ttu-id="81d88-107">Description</span><span class="sxs-lookup"><span data-stu-id="81d88-107">Description</span></span>                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="81d88-108"><span id="radian"></span><span id="RADIAN"></span>弧度</span><span class="sxs-lookup"><span data-stu-id="81d88-108"><span id="radian"></span><span id="RADIAN"></span>radian</span></span><br/> | <span data-ttu-id="81d88-109">要轉換成度數的值（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="81d88-109">The value, in radians, to convert to degrees.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="81d88-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="81d88-110">Return Value</span></span>

<span data-ttu-id="81d88-111">宏會傳回弧度值（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="81d88-111">The macro returns the radian value in degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d88-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="81d88-112">Requirements</span></span>



| <span data-ttu-id="81d88-113">需求</span><span class="sxs-lookup"><span data-stu-id="81d88-113">Requirement</span></span> | <span data-ttu-id="81d88-114">值</span><span class="sxs-lookup"><span data-stu-id="81d88-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81d88-115">標頭</span><span class="sxs-lookup"><span data-stu-id="81d88-115">Header</span></span><br/> | <dl> <span data-ttu-id="81d88-116"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="81d88-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d88-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81d88-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d88-118">巨集</span><span class="sxs-lookup"><span data-stu-id="81d88-118">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="81d88-119">**D3DXToRadian**</span><span class="sxs-lookup"><span data-stu-id="81d88-119">**D3DXToRadian**</span></span>](d3dxtoradian.md)
</dt> <dt>

[<span data-ttu-id="81d88-120">D3DX \_ PI</span><span class="sxs-lookup"><span data-stu-id="81d88-120">D3DX\_PI</span></span>](other-d3dx-constants.md)
</dt> </dl>

 

 




