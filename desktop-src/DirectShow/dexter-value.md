---
description: 識別要在轉換或效果上設定的屬性，以及屬性在轉換或效果期間所採用的相異值數目。
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: 'DEXTER_VALUE 結構 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999262"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="db09c-103">DEXTER \_ 值結構</span><span class="sxs-lookup"><span data-stu-id="db09c-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="db09c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="db09c-104">\[Deprecated.</span></span> <span data-ttu-id="db09c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="db09c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="db09c-106">識別要在轉換或效果上設定的屬性，以及屬性在轉換或效果期間所採用的相異值數目。</span><span class="sxs-lookup"><span data-stu-id="db09c-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="db09c-107">語法</span><span class="sxs-lookup"><span data-stu-id="db09c-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="db09c-108">成員</span><span class="sxs-lookup"><span data-stu-id="db09c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="db09c-109">**V**</span><span class="sxs-lookup"><span data-stu-id="db09c-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="db09c-110">屬性的值。</span><span class="sxs-lookup"><span data-stu-id="db09c-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="db09c-111">**Rt**</span><span class="sxs-lookup"><span data-stu-id="db09c-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="db09c-112">屬性假設值的時間（相對於轉換或效果的開頭）。</span><span class="sxs-lookup"><span data-stu-id="db09c-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="db09c-113">**dwInterp**</span><span class="sxs-lookup"><span data-stu-id="db09c-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="db09c-114">旗標，指出屬性如何從先前的值到此值之間的進展。</span><span class="sxs-lookup"><span data-stu-id="db09c-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="db09c-115">必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="db09c-115">Must be one of the following:</span></span>



| <span data-ttu-id="db09c-116">值</span><span class="sxs-lookup"><span data-stu-id="db09c-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="db09c-117">意義</span><span class="sxs-lookup"><span data-stu-id="db09c-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="db09c-118"><dt>**DEXTERF \_ 跳躍**</dt></span><span class="sxs-lookup"><span data-stu-id="db09c-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="db09c-119">屬性會立即跳到指定時間的新值。</span><span class="sxs-lookup"><span data-stu-id="db09c-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="db09c-120"><dt>**DEXTERF \_ 插補**</dt></span><span class="sxs-lookup"><span data-stu-id="db09c-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="db09c-121">屬性是從上一個值的一段時間內呈線性插補。</span><span class="sxs-lookup"><span data-stu-id="db09c-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db09c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="db09c-122">Requirements</span></span>



| <span data-ttu-id="db09c-123">需求</span><span class="sxs-lookup"><span data-stu-id="db09c-123">Requirement</span></span> | <span data-ttu-id="db09c-124">值</span><span class="sxs-lookup"><span data-stu-id="db09c-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db09c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="db09c-125">Header</span></span><br/> | <dl> <span data-ttu-id="db09c-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="db09c-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db09c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db09c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db09c-128">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="db09c-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="db09c-129">**DEXTER \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="db09c-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




