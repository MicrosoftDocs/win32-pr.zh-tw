---
description: 包含紅色、綠色和藍色的斜坡資料。
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: 'D3DGAMMARAMP 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979879"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="191a5-103">D3DGAMMARAMP 結構</span><span class="sxs-lookup"><span data-stu-id="191a5-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="191a5-104">包含紅色、綠色和藍色的斜坡資料。</span><span class="sxs-lookup"><span data-stu-id="191a5-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="191a5-105">語法</span><span class="sxs-lookup"><span data-stu-id="191a5-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="191a5-106">成員</span><span class="sxs-lookup"><span data-stu-id="191a5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="191a5-107">**紅**</span><span class="sxs-lookup"><span data-stu-id="191a5-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="191a5-108">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="191a5-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="191a5-109">描述 red gamma 曲線的 256 WORD 元素陣列。</span><span class="sxs-lookup"><span data-stu-id="191a5-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="191a5-110">**綠色**</span><span class="sxs-lookup"><span data-stu-id="191a5-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="191a5-111">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="191a5-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="191a5-112">描述綠色 gamma 曲線的 256 WORD 元素陣列。</span><span class="sxs-lookup"><span data-stu-id="191a5-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="191a5-113">**藍色**</span><span class="sxs-lookup"><span data-stu-id="191a5-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="191a5-114">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="191a5-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="191a5-115">描述藍色 gamma 曲線的 256 WORD 元素陣列。</span><span class="sxs-lookup"><span data-stu-id="191a5-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="191a5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="191a5-116">Requirements</span></span>



| <span data-ttu-id="191a5-117">需求</span><span class="sxs-lookup"><span data-stu-id="191a5-117">Requirement</span></span> | <span data-ttu-id="191a5-118">值</span><span class="sxs-lookup"><span data-stu-id="191a5-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="191a5-119">標頭</span><span class="sxs-lookup"><span data-stu-id="191a5-119">Header</span></span><br/> | <dl> <span data-ttu-id="191a5-120"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="191a5-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191a5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="191a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191a5-122">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="191a5-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="191a5-123">**GetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="191a5-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="191a5-124">**SetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="191a5-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
