---
title: WMDM_PROP_VALUES_ENUM 結構
description: WMDM \_ \_ \_ 屬性值列舉結構包含特定屬性設定中特定屬性的有效值列舉集合。
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001542"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="335a4-104">WMDM \_ 的 \_ 值 \_ 列舉結構</span><span class="sxs-lookup"><span data-stu-id="335a4-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="335a4-105">**WMDM 屬性 \_ \_ 值 \_ 列舉** 結構包含特定屬性設定中特定屬性的有效值列舉集合。</span><span class="sxs-lookup"><span data-stu-id="335a4-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="335a4-106">語法</span><span class="sxs-lookup"><span data-stu-id="335a4-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="335a4-107">成員</span><span class="sxs-lookup"><span data-stu-id="335a4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="335a4-108">**cEnumValues**</span><span class="sxs-lookup"><span data-stu-id="335a4-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="335a4-109">列舉值的計數。</span><span class="sxs-lookup"><span data-stu-id="335a4-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="335a4-110">**pValues**</span><span class="sxs-lookup"><span data-stu-id="335a4-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="335a4-111">值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="335a4-111">Pointer to an array of values.</span></span> <span data-ttu-id="335a4-112">陣列的大小等於 **cEnumValues** 的值。</span><span class="sxs-lookup"><span data-stu-id="335a4-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="335a4-113">備註</span><span class="sxs-lookup"><span data-stu-id="335a4-113">Remarks</span></span>

<span data-ttu-id="335a4-114">此結構會在 WMDM 的 [描述] **\_ \_ DESC** 結構中用來描述有效值的列舉集合。</span><span class="sxs-lookup"><span data-stu-id="335a4-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="335a4-115">\_ \_ \_ \_ \_ 從 WMDM 列舉配置有效值（列舉為 **\_ 有效值） \_ \_ \_ \_ 表單** 列舉中選取了 WMDM 列舉配置值的列舉值時，可使用一組列舉的有效值。</span><span class="sxs-lookup"><span data-stu-id="335a4-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="335a4-116">需要呼叫端才能釋放 **pValues** 所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="335a4-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="335a4-117">如需如何進行這項操作的範例，請參閱 [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)。</span><span class="sxs-lookup"><span data-stu-id="335a4-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="335a4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="335a4-118">Requirements</span></span>



| <span data-ttu-id="335a4-119">需求</span><span class="sxs-lookup"><span data-stu-id="335a4-119">Requirement</span></span> | <span data-ttu-id="335a4-120">值</span><span class="sxs-lookup"><span data-stu-id="335a4-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="335a4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="335a4-121">Header</span></span><br/> | <dl> <span data-ttu-id="335a4-122"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="335a4-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="335a4-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="335a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="335a4-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="335a4-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="335a4-125">**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 形式**</span><span class="sxs-lookup"><span data-stu-id="335a4-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="335a4-126">**WMDM \_ 格式 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="335a4-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="335a4-127">**WMDM \_ \_ 配置設定**</span><span class="sxs-lookup"><span data-stu-id="335a4-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="335a4-128">**WMDM 的一種 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="335a4-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="335a4-129">**WMDM \_ 的 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="335a4-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="335a4-130">**結構**</span><span class="sxs-lookup"><span data-stu-id="335a4-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





