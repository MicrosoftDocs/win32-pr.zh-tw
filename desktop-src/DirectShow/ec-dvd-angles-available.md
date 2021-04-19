---
description: 指出是否現正播放角度區塊，以及是否可以執行角度變更。
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: 'EC_DVD_ANGLES_AVAILABLE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993216"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="5c9cf-103">EC \_ DVD \_ 角度 \_ 可用</span><span class="sxs-lookup"><span data-stu-id="5c9cf-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="5c9cf-104">指出是否現正播放角度區塊，以及是否可以執行角度變更。</span><span class="sxs-lookup"><span data-stu-id="5c9cf-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c9cf-105">參數</span><span class="sxs-lookup"><span data-stu-id="5c9cf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c9cf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5c9cf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5c9cf-107">布林值 (**BOOL**) 值，指出是否現正播放角區塊。</span><span class="sxs-lookup"><span data-stu-id="5c9cf-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="5c9cf-108">零 (0) 表示播放不在角度區塊中，而且無法使用角度，一個 (1) 表示現正播放角度區塊，且可以執行角度變更。</span><span class="sxs-lookup"><span data-stu-id="5c9cf-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="5c9cf-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5c9cf-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5c9cf-110">零個。</span><span class="sxs-lookup"><span data-stu-id="5c9cf-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c9cf-111">備註</span><span class="sxs-lookup"><span data-stu-id="5c9cf-111">Remarks</span></span>

<span data-ttu-id="5c9cf-112">角度變化不限於角度區塊，而角度變化的變化只會在角度區塊中看到。</span><span class="sxs-lookup"><span data-stu-id="5c9cf-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9cf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c9cf-113">Requirements</span></span>



| <span data-ttu-id="5c9cf-114">需求</span><span class="sxs-lookup"><span data-stu-id="5c9cf-114">Requirement</span></span> | <span data-ttu-id="5c9cf-115">值</span><span class="sxs-lookup"><span data-stu-id="5c9cf-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9cf-116">標頭</span><span class="sxs-lookup"><span data-stu-id="5c9cf-116">Header</span></span><br/> | <dl> <span data-ttu-id="5c9cf-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="5c9cf-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9cf-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c9cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9cf-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="5c9cf-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="5c9cf-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="5c9cf-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5c9cf-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="5c9cf-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




