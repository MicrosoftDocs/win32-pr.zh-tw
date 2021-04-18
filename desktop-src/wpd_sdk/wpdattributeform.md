---
description: WpdAttributeForm 列舉型別描述屬性如何儲存其值。
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: 'WpdAttributeForm 列舉 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976272"
---
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="f1ad6-103">WpdAttributeForm 列舉</span><span class="sxs-lookup"><span data-stu-id="f1ad6-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="f1ad6-104">**WpdAttributeForm** 列舉型別描述屬性如何儲存其值。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ad6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1ad6-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="f1ad6-106">常數</span><span class="sxs-lookup"><span data-stu-id="f1ad6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f1ad6-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_ \_ 未指定 WPD 屬性屬性 \_ 表單 \_**</span><span class="sxs-lookup"><span data-stu-id="f1ad6-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="f1ad6-108">未指定屬性資料的格式。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad6-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="f1ad6-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f1ad6-110">值是以值的範圍表示，最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad6-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="f1ad6-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="f1ad6-112">屬性有一系列的個別值。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad6-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 正則 \_ 運算式**</span><span class="sxs-lookup"><span data-stu-id="f1ad6-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="f1ad6-114">屬性值是正則運算式，而不是常值運算式。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="f1ad6-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD \_ 屬性 \_ 屬性 \_ 表單 \_ 物件 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f1ad6-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="f1ad6-116">屬性值代表物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1ad6-117">備註</span><span class="sxs-lookup"><span data-stu-id="f1ad6-117">Remarks</span></span>

<span data-ttu-id="f1ad6-118">[WPD \_ 屬性 \_ 屬性 \_ 表單](attributes.md)屬性會使用這個列舉來描述屬性資料的儲存方式。</span><span class="sxs-lookup"><span data-stu-id="f1ad6-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ad6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1ad6-119">Requirements</span></span>



| <span data-ttu-id="f1ad6-120">需求</span><span class="sxs-lookup"><span data-stu-id="f1ad6-120">Requirement</span></span> | <span data-ttu-id="f1ad6-121">值</span><span class="sxs-lookup"><span data-stu-id="f1ad6-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ad6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f1ad6-122">Header</span></span><br/> | <dl> <span data-ttu-id="f1ad6-123"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1ad6-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ad6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1ad6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ad6-125">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="f1ad6-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




