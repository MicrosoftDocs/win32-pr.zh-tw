---
description: WPD \_ 裁剪的 \_ 狀態值 \_ 列舉型別描述影像的裁剪狀態。
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: 'WPD_CROPPED_STATUS_VALUES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982263"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="db49d-103">WPD \_ 裁剪的 \_ 狀態值 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="db49d-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="db49d-104">**WPD \_ 裁剪的 \_ 狀態值 \_** 列舉型別描述影像的裁剪狀態。</span><span class="sxs-lookup"><span data-stu-id="db49d-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="db49d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db49d-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="db49d-106">常數</span><span class="sxs-lookup"><span data-stu-id="db49d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="db49d-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_ \_ \_ 未裁剪的 WPD 裁剪狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="db49d-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="db49d-108">尚未裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="db49d-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="db49d-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**裁剪的 WPD \_ 裁剪 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="db49d-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="db49d-110">影像已裁剪。</span><span class="sxs-lookup"><span data-stu-id="db49d-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="db49d-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_ \_ \_ \_ 不應 \_ \_ 裁剪 WPD 裁剪的狀態**</span><span class="sxs-lookup"><span data-stu-id="db49d-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="db49d-112">影像尚未經過，也不應該裁剪。</span><span class="sxs-lookup"><span data-stu-id="db49d-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db49d-113">備註</span><span class="sxs-lookup"><span data-stu-id="db49d-113">Remarks</span></span>

<span data-ttu-id="db49d-114">指出影像的裁剪狀態。</span><span class="sxs-lookup"><span data-stu-id="db49d-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="db49d-115">[WPD \_ 影像 \_ 裁剪 \_ 狀態](image-properties.md)屬性會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="db49d-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="db49d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="db49d-116">Requirements</span></span>



| <span data-ttu-id="db49d-117">需求</span><span class="sxs-lookup"><span data-stu-id="db49d-117">Requirement</span></span> | <span data-ttu-id="db49d-118">值</span><span class="sxs-lookup"><span data-stu-id="db49d-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="db49d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="db49d-119">Header</span></span><br/> | <dl> <span data-ttu-id="db49d-120"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="db49d-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db49d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db49d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db49d-122">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="db49d-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




