---
description: 將度數轉換成弧度。
ms.assetid: 450806bd-db2f-47be-ae80-c261088b1bb8
title: 'D3DXToRadian (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToRadian
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: e06184a0d3c654a2c0e82431ff25a339f5682837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999006"
---
# <a name="d3dxtoradian"></a><span data-ttu-id="03d11-103">D3DXToRadian</span><span class="sxs-lookup"><span data-stu-id="03d11-103">D3DXToRadian</span></span>

<span data-ttu-id="03d11-104">將度數轉換成弧度。</span><span class="sxs-lookup"><span data-stu-id="03d11-104">Converts degrees into radians.</span></span>

``` syntax
#define D3DXToRadian(degree) ((degree) * (D3DX_PI / 180.0f))
```

## <a name="parameters"></a><span data-ttu-id="03d11-105">參數</span><span class="sxs-lookup"><span data-stu-id="03d11-105">Parameters</span></span>



| <span data-ttu-id="03d11-106">參數</span><span class="sxs-lookup"><span data-stu-id="03d11-106">Parameter</span></span>                                                           | <span data-ttu-id="03d11-107">Description</span><span class="sxs-lookup"><span data-stu-id="03d11-107">Description</span></span>                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="03d11-108"><span id="degree"></span><span id="DEGREE"></span>程度</span><span class="sxs-lookup"><span data-stu-id="03d11-108"><span id="degree"></span><span id="DEGREE"></span>degree</span></span><br/> | <span data-ttu-id="03d11-109">要轉換成弧度的值（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="03d11-109">The value, in degrees, to convert to radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="03d11-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="03d11-110">Return Value</span></span>

<span data-ttu-id="03d11-111">宏會傳回以弧度為單位的度值。</span><span class="sxs-lookup"><span data-stu-id="03d11-111">The macro returns the degree value in radians.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d11-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="03d11-112">Requirements</span></span>



| <span data-ttu-id="03d11-113">需求</span><span class="sxs-lookup"><span data-stu-id="03d11-113">Requirement</span></span> | <span data-ttu-id="03d11-114">值</span><span class="sxs-lookup"><span data-stu-id="03d11-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03d11-115">標頭</span><span class="sxs-lookup"><span data-stu-id="03d11-115">Header</span></span><br/> | <dl> <span data-ttu-id="03d11-116"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="03d11-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d11-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03d11-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d11-118">巨集</span><span class="sxs-lookup"><span data-stu-id="03d11-118">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="03d11-119">**D3DXToDegree**</span><span class="sxs-lookup"><span data-stu-id="03d11-119">**D3DXToDegree**</span></span>](d3dxtodegree.md)
</dt> <dt>

[<span data-ttu-id="03d11-120">D3DX \_ PI</span><span class="sxs-lookup"><span data-stu-id="03d11-120">D3DX\_PI</span></span>](other-d3dx-constants.md)
</dt> </dl>

 

 




