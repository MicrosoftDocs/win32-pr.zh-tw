---
description: 發出 DVD 錯誤狀況信號。
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: 'EC_DVD_ERROR (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989553"
---
# <a name="ec_dvd_error"></a><span data-ttu-id="7d450-103">EC \_ DVD \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="7d450-103">EC\_DVD\_ERROR</span></span>

<span data-ttu-id="7d450-104">發出 DVD 錯誤狀況信號。</span><span class="sxs-lookup"><span data-stu-id="7d450-104">Signals a DVD error condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d450-105">參數</span><span class="sxs-lookup"><span data-stu-id="7d450-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d450-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7d450-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7d450-107">表示錯誤狀況的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="7d450-107">**DWORD** value indicating the error condition.</span></span> <span data-ttu-id="7d450-108">[**DVD \_ 錯誤**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error)列舉資料類型的成員。</span><span class="sxs-lookup"><span data-stu-id="7d450-108">Member of the [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="7d450-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7d450-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7d450-110">意義取決於 *lParam1* 的值。</span><span class="sxs-lookup"><span data-stu-id="7d450-110">Meaning depends on the value of *lParam1*.</span></span> <span data-ttu-id="7d450-111">如需詳細資訊，請參閱 [**DVD \_ 錯誤**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) 。</span><span class="sxs-lookup"><span data-stu-id="7d450-111">See [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d450-112">備註</span><span class="sxs-lookup"><span data-stu-id="7d450-112">Remarks</span></span>

<span data-ttu-id="7d450-113">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="7d450-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d450-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d450-114">Requirements</span></span>



| <span data-ttu-id="7d450-115">需求</span><span class="sxs-lookup"><span data-stu-id="7d450-115">Requirement</span></span> | <span data-ttu-id="7d450-116">值</span><span class="sxs-lookup"><span data-stu-id="7d450-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d450-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7d450-117">Header</span></span><br/> | <dl> <span data-ttu-id="7d450-118"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="7d450-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d450-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d450-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d450-120">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="7d450-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7d450-121">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="7d450-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7d450-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="7d450-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




