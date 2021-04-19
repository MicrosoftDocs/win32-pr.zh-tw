---
description: 發出 DVD 警告條件的信號。
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: 'EC_DVD_WARNING (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995641"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="54780-103">EC \_ DVD \_ 警告</span><span class="sxs-lookup"><span data-stu-id="54780-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="54780-104">發出 DVD 警告條件的信號。</span><span class="sxs-lookup"><span data-stu-id="54780-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="54780-105">參數</span><span class="sxs-lookup"><span data-stu-id="54780-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54780-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="54780-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="54780-107">指出警告條件的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="54780-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="54780-108">[**DVD \_ 警告**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning)列舉資料類型的成員。</span><span class="sxs-lookup"><span data-stu-id="54780-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="54780-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="54780-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="54780-110">如果 *pParam1* 等於 DVD \_ 警告 \_ 開啟、DVD \_ 警告 \_ 搜尋或 dvd \_ 警告 \_ 讀取，則 *lParam2* 包含最後從 **GetLastError** 傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="54780-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54780-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="54780-111">Requirements</span></span>



| <span data-ttu-id="54780-112">需求</span><span class="sxs-lookup"><span data-stu-id="54780-112">Requirement</span></span> | <span data-ttu-id="54780-113">值</span><span class="sxs-lookup"><span data-stu-id="54780-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54780-114">標頭</span><span class="sxs-lookup"><span data-stu-id="54780-114">Header</span></span><br/> | <dl> <span data-ttu-id="54780-115"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="54780-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54780-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54780-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54780-117">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="54780-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="54780-118">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="54780-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="54780-119">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="54780-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




