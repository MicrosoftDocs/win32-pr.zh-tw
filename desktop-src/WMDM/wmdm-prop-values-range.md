---
title: WMDM_PROP_VALUES_RANGE 結構
description: WMDM 屬性 \_ \_ 值 \_ 範圍結構描述特定屬性設定中特定屬性的有效值範圍。
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992811"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="1d9e5-104">WMDM \_ 的 \_ 值 \_ 範圍結構</span><span class="sxs-lookup"><span data-stu-id="1d9e5-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="1d9e5-105">**WMDM 屬性 \_ \_ 值 \_ 範圍** 結構描述特定屬性設定中特定屬性的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9e5-106">語法</span><span class="sxs-lookup"><span data-stu-id="1d9e5-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="1d9e5-107">成員</span><span class="sxs-lookup"><span data-stu-id="1d9e5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d9e5-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="1d9e5-109">範圍中的最小值。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="1d9e5-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="1d9e5-111">範圍中的最大值。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="1d9e5-112">**rangeStep**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="1d9e5-113">有效值從最小值遞增為最大值的步驟大小。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="1d9e5-114">這允許在範圍內指定離散的允許值。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d9e5-115">備註</span><span class="sxs-lookup"><span data-stu-id="1d9e5-115">Remarks</span></span>

<span data-ttu-id="1d9e5-116">此結構會在 WMDM 的 [描述] [**\_ \_ DESC**](wmdm-prop-desc.md) 結構中用來描述有效值的範圍。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="1d9e5-117">\_ \_ \_ \_ \_ 從 [**WMDM 列舉值的有效值（列舉 \_ 值） \_ \_ \_ \_ 表單**](wmdm-enum-prop-valid-values-form.md)列舉中選取了 WMDM 列舉類型的有效值時，可使用有效的值範圍。</span><span class="sxs-lookup"><span data-stu-id="1d9e5-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d9e5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d9e5-118">Requirements</span></span>



| <span data-ttu-id="1d9e5-119">需求</span><span class="sxs-lookup"><span data-stu-id="1d9e5-119">Requirement</span></span> | <span data-ttu-id="1d9e5-120">值</span><span class="sxs-lookup"><span data-stu-id="1d9e5-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9e5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1d9e5-121">Header</span></span><br/> | <dl> <span data-ttu-id="1d9e5-122"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e5-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d9e5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d9e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d9e5-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="1d9e5-125">**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 形式**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="1d9e5-126">**WMDM \_ 格式 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="1d9e5-127">**WMDM \_ \_ 配置設定**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="1d9e5-128">**WMDM 的一種 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="1d9e5-129">**WMDM 的 \_ 主張 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="1d9e5-130">**結構**</span><span class="sxs-lookup"><span data-stu-id="1d9e5-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





