---
description: WPD 的 \_ 白色 \_ 餘額 \_ 設定列舉類型會說明影片或影像裝置如何加權色彩，以達到適當的白色平衡。
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: 'WPD_WHITE_BALANCE_SETTINGS 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994671"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="8def6-103">WPD \_ 白色 \_ 餘額 \_ 設定列舉</span><span class="sxs-lookup"><span data-stu-id="8def6-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="8def6-104">**WPD 的 \_ 白色 \_ 餘額 \_ 設定** 列舉類型會說明影片或影像裝置如何加權色彩，以達到適當的白色平衡。</span><span class="sxs-lookup"><span data-stu-id="8def6-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="8def6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8def6-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="8def6-106">常數</span><span class="sxs-lookup"><span data-stu-id="8def6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8def6-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_未定義的 WPD 白色 \_ 餘額 \_**</span><span class="sxs-lookup"><span data-stu-id="8def6-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-108">尚未定義此值。</span><span class="sxs-lookup"><span data-stu-id="8def6-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="8def6-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD \_ 白色 \_ 餘額 \_ 手動**</span><span class="sxs-lookup"><span data-stu-id="8def6-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-110">您可以使用 [WPD \_ 靜止 \_ 影像 \_ RGB \_ 增益](still-image-properties.md) 屬性來明確設定白色餘額，而且也不會自行變更。</span><span class="sxs-lookup"><span data-stu-id="8def6-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="8def6-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_自動 WPD 白色 \_ 餘額 \_**</span><span class="sxs-lookup"><span data-stu-id="8def6-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-112">裝置會設定白色餘額。</span><span class="sxs-lookup"><span data-stu-id="8def6-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="8def6-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD \_ 白色 \_ 平衡 \_ 一個 \_ 推播 \_ 自動**</span><span class="sxs-lookup"><span data-stu-id="8def6-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-114">裝置會設定白色餘額，但只有當使用者推送裝置的 [捕捉] 按鈕時，才會將裝置用於白色欄位。</span><span class="sxs-lookup"><span data-stu-id="8def6-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="8def6-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ 白色 \_ 餘額 \_ 日光**</span><span class="sxs-lookup"><span data-stu-id="8def6-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-116">裝置將使用適用于大部分日光設定的白色餘額號碼。</span><span class="sxs-lookup"><span data-stu-id="8def6-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="8def6-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ 白色 \_ 餘額 \_ TUNGSTEN**</span><span class="sxs-lookup"><span data-stu-id="8def6-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-118">裝置將使用適用于大部分室內 incandescent 光源設定的白色餘額號碼。</span><span class="sxs-lookup"><span data-stu-id="8def6-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="8def6-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD \_ 白色 \_ 餘額 \_ FLASH**</span><span class="sxs-lookup"><span data-stu-id="8def6-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="8def6-120">裝置將使用適合搭配 flash 使用的白色餘額號碼。</span><span class="sxs-lookup"><span data-stu-id="8def6-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8def6-121">備註</span><span class="sxs-lookup"><span data-stu-id="8def6-121">Remarks</span></span>

<span data-ttu-id="8def6-122">[WPD \_ 仍 \_ 影像的 \_ 白色 \_ 餘額](still-image-properties.md)屬性會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="8def6-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8def6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8def6-123">Requirements</span></span>



| <span data-ttu-id="8def6-124">需求</span><span class="sxs-lookup"><span data-stu-id="8def6-124">Requirement</span></span> | <span data-ttu-id="8def6-125">值</span><span class="sxs-lookup"><span data-stu-id="8def6-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8def6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8def6-126">Header</span></span><br/> | <dl> <span data-ttu-id="8def6-127"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="8def6-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8def6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8def6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8def6-129">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="8def6-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




