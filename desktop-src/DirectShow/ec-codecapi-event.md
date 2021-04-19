---
description: EC \_ CODECAPI \_ 事件事件是由編碼器傳送以表示編碼事件。 用戶端會藉由呼叫 ICodecAPI：： RegisterForEvent 方法來註冊編碼器事件。
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: 'EC_CODECAPI_EVENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995761"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="cbec5-104">EC \_ CODECAPI \_ 活動</span><span class="sxs-lookup"><span data-stu-id="cbec5-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="cbec5-105">EC \_ CODECAPI \_ 事件事件是由編碼器傳送以表示編碼事件。</span><span class="sxs-lookup"><span data-stu-id="cbec5-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="cbec5-106">用戶端會藉由呼叫 [**ICodecAPI：： RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) 方法來註冊編碼器事件。</span><span class="sxs-lookup"><span data-stu-id="cbec5-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbec5-107">參數</span><span class="sxs-lookup"><span data-stu-id="cbec5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbec5-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cbec5-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cbec5-109">使用者資料。</span><span class="sxs-lookup"><span data-stu-id="cbec5-109">User data.</span></span> <span data-ttu-id="cbec5-110">此參數的值是呼叫端在 [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent)方法的 *userData* 參數中指定的指標。</span><span class="sxs-lookup"><span data-stu-id="cbec5-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="cbec5-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cbec5-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cbec5-112">事件資料的指標。</span><span class="sxs-lookup"><span data-stu-id="cbec5-112">Pointer to the event data.</span></span> <span data-ttu-id="cbec5-113">這項資料是由編碼器所配置，且必須由應用程式使用 **CoTaskMemFree** 函式來釋放。</span><span class="sxs-lookup"><span data-stu-id="cbec5-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="cbec5-114">資料區塊會以 [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) 結構開始;將 *lParam2* 參數轉換為此結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cbec5-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="cbec5-115">預設動作</span><span class="sxs-lookup"><span data-stu-id="cbec5-115">Default Action</span></span>

<span data-ttu-id="cbec5-116">沒有預設動作。</span><span class="sxs-lookup"><span data-stu-id="cbec5-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbec5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbec5-117">Requirements</span></span>



| <span data-ttu-id="cbec5-118">需求</span><span class="sxs-lookup"><span data-stu-id="cbec5-118">Requirement</span></span> | <span data-ttu-id="cbec5-119">值</span><span class="sxs-lookup"><span data-stu-id="cbec5-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cbec5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cbec5-120">Header</span></span><br/> | <dl> <span data-ttu-id="cbec5-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbec5-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbec5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbec5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbec5-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="cbec5-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cbec5-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="cbec5-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




