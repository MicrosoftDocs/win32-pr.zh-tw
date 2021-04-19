---
title: WMDM_ENUM_PROP_VALID_VALUES_FORM 列舉
description: WMDM \_ 列舉 \_ \_ 屬性有效的 \_ 值 \_ 表單列舉型別描述了可能的屬性有效值形式。
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982271"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="44851-104">WMDM \_ 列舉 \_ \_ 值的 \_ 有效值 \_ 表單列舉</span><span class="sxs-lookup"><span data-stu-id="44851-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="44851-105">**WMDM \_ 列舉屬性 \_ 有效 \_ 的 \_ 值 \_ 表單** 列舉型別描述了可能的屬性有效值形式。</span><span class="sxs-lookup"><span data-stu-id="44851-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="44851-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="44851-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="44851-107">常數</span><span class="sxs-lookup"><span data-stu-id="44851-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="44851-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ 列舉會將 \_ 有效值的 \_ 有效值 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44851-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="44851-109">所有值都是有效的。</span><span class="sxs-lookup"><span data-stu-id="44851-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="44851-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="44851-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="44851-111">有效的值會以範圍表示。</span><span class="sxs-lookup"><span data-stu-id="44851-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="44851-112">如需詳細資訊，請參閱 WMDM 的「 [**\_ \_ 值 \_ 範圍**](wmdm-prop-values-range.md) 結構」。</span><span class="sxs-lookup"><span data-stu-id="44851-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="44851-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM \_ 列舉 \_ 的 \_ 有效 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="44851-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="44851-114">有效的值為列舉集合。</span><span class="sxs-lookup"><span data-stu-id="44851-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="44851-115">如需詳細資訊，請參閱 WMDM 的「內容」 [**\_ \_ 值 \_ 列舉**](wmdm-prop-values-enum.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="44851-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44851-116">備註</span><span class="sxs-lookup"><span data-stu-id="44851-116">Remarks</span></span>

<span data-ttu-id="44851-117">[**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md)結構中會使用這個列舉來指定屬性的有效值格式。</span><span class="sxs-lookup"><span data-stu-id="44851-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="44851-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="44851-118">Requirements</span></span>



| <span data-ttu-id="44851-119">需求</span><span class="sxs-lookup"><span data-stu-id="44851-119">Requirement</span></span> | <span data-ttu-id="44851-120">值</span><span class="sxs-lookup"><span data-stu-id="44851-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44851-121">標頭</span><span class="sxs-lookup"><span data-stu-id="44851-121">Header</span></span><br/> | <dl> <span data-ttu-id="44851-122"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="44851-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44851-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44851-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44851-124">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="44851-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="44851-125">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="44851-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="44851-126">**WMDM \_ 格式 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="44851-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="44851-127">**WMDM \_ \_ 配置設定**</span><span class="sxs-lookup"><span data-stu-id="44851-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="44851-128">**WMDM 的一種 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="44851-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="44851-129">**WMDM 的 \_ 主張 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="44851-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="44851-130">**WMDM \_ 的 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="44851-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





