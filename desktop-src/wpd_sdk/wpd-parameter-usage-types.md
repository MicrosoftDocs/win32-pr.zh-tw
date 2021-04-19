---
description: WPD \_ 參數 \_ 使用 \_ 類型列舉類型會描述如何在指定方法中使用方法參數。
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: 'WPD_PARAMETER_USAGE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994659"
---
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="00744-103">WPD \_ 參數 \_ 使用 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="00744-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="00744-104">[**WPD \_ 參數 \_ 使用 \_ 類型**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types)列舉類型會描述如何在指定方法中使用方法參數。</span><span class="sxs-lookup"><span data-stu-id="00744-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00744-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00744-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="00744-106">常數</span><span class="sxs-lookup"><span data-stu-id="00744-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00744-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD \_ 參數 \_ 使用方式傳回 \_**</span><span class="sxs-lookup"><span data-stu-id="00744-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="00744-108">參數會接收傳回值（如果是由方法指定）。</span><span class="sxs-lookup"><span data-stu-id="00744-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="00744-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD \_ 參數 \_ 使用 \_ 方式**</span><span class="sxs-lookup"><span data-stu-id="00744-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="00744-110">參數會在呼叫方法之前包含輸入值。</span><span class="sxs-lookup"><span data-stu-id="00744-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="00744-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD \_ 參數 \_ 使用 \_ 方式**</span><span class="sxs-lookup"><span data-stu-id="00744-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="00744-112">此參數包含方法傳回時的輸出值。</span><span class="sxs-lookup"><span data-stu-id="00744-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="00744-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD \_ 參數 \_ 使用方式 \_ INOUT**</span><span class="sxs-lookup"><span data-stu-id="00744-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="00744-114">參數包含在呼叫方法之前的輸入值，以及傳回時的輸出值。</span><span class="sxs-lookup"><span data-stu-id="00744-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00744-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="00744-115">Requirements</span></span>



| <span data-ttu-id="00744-116">需求</span><span class="sxs-lookup"><span data-stu-id="00744-116">Requirement</span></span> | <span data-ttu-id="00744-117">值</span><span class="sxs-lookup"><span data-stu-id="00744-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="00744-118">標頭</span><span class="sxs-lookup"><span data-stu-id="00744-118">Header</span></span><br/> | <dl> <span data-ttu-id="00744-119"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="00744-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

