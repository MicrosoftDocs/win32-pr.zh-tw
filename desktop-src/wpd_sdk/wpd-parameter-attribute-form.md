---
description: 描述 (方法或事件) 參數如何儲存其值。
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: 'WpdParameterAttributeForm 列舉 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989513"
---
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="86065-103">WpdParameterAttributeForm 列舉</span><span class="sxs-lookup"><span data-stu-id="86065-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="86065-104">[**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85))列舉型別描述 (方法或事件) 參數如何儲存其值。</span><span class="sxs-lookup"><span data-stu-id="86065-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="86065-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86065-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="86065-106">常數</span><span class="sxs-lookup"><span data-stu-id="86065-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="86065-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**\_ \_ 未指定 WPD 參數屬性 \_ 表單 \_**</span><span class="sxs-lookup"><span data-stu-id="86065-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="86065-108">未指定參數的格式。</span><span class="sxs-lookup"><span data-stu-id="86065-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="86065-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD \_ 參數 \_ 屬性 \_ 表單 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="86065-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="86065-110">參數會指定範圍。</span><span class="sxs-lookup"><span data-stu-id="86065-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="86065-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD \_ 參數 \_ 屬性 \_ 表單 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="86065-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="86065-112">參數是列舉。</span><span class="sxs-lookup"><span data-stu-id="86065-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="86065-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD \_ 參數 \_ 屬性 \_ 表單 \_ 正則 \_ 運算式**</span><span class="sxs-lookup"><span data-stu-id="86065-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="86065-114">參數是正則運算式。</span><span class="sxs-lookup"><span data-stu-id="86065-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="86065-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD \_ 參數 \_ 屬性 \_ 物件 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="86065-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="86065-116">參數是物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="86065-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86065-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="86065-117">Requirements</span></span>



| <span data-ttu-id="86065-118">需求</span><span class="sxs-lookup"><span data-stu-id="86065-118">Requirement</span></span> | <span data-ttu-id="86065-119">值</span><span class="sxs-lookup"><span data-stu-id="86065-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="86065-120">標頭</span><span class="sxs-lookup"><span data-stu-id="86065-120">Header</span></span><br/> | <dl> <span data-ttu-id="86065-121"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="86065-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

