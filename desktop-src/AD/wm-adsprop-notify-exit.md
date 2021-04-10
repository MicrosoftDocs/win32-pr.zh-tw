---
title: 'WM_ADSPROP_NOTIFY_EXIT 訊息 (Adsprop .h) '
description: 當不再需要通知物件時，Active Directory 的屬性工作表延伸會將 WM \_ ADSPROP \_ 通知結束訊息傳送 \_ 給通知物件。
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934920"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="e07db-104">WM \_ ADSPROP \_ 通知結束 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="e07db-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="e07db-105">當不再需要通知物件時，Active Directory 的屬性工作表延伸會將 **WM \_ ADSPROP \_ 通知 \_** 結束訊息傳送給通知物件。</span><span class="sxs-lookup"><span data-stu-id="e07db-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="e07db-106">參數</span><span class="sxs-lookup"><span data-stu-id="e07db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07db-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="e07db-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e07db-108">通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e07db-108">The handle of the notification object.</span></span> <span data-ttu-id="e07db-109">若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。</span><span class="sxs-lookup"><span data-stu-id="e07db-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="e07db-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e07db-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e07db-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="e07db-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e07db-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e07db-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e07db-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="e07db-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07db-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e07db-114">Return value</span></span>

<span data-ttu-id="e07db-115">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e07db-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e07db-116">備註</span><span class="sxs-lookup"><span data-stu-id="e07db-116">Remarks</span></span>

<span data-ttu-id="e07db-117">通知物件將會自行刪除以回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="e07db-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="e07db-118">傳送此訊息時，應該將通知物件控制碼視為無效。</span><span class="sxs-lookup"><span data-stu-id="e07db-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="e07db-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e07db-119">Requirements</span></span>



| <span data-ttu-id="e07db-120">需求</span><span class="sxs-lookup"><span data-stu-id="e07db-120">Requirement</span></span> | <span data-ttu-id="e07db-121">值</span><span class="sxs-lookup"><span data-stu-id="e07db-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e07db-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e07db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e07db-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e07db-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="e07db-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e07db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e07db-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e07db-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="e07db-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e07db-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07db-127"><dt>Adsprop。h</dt></span><span class="sxs-lookup"><span data-stu-id="e07db-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07db-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e07db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07db-129">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="e07db-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="e07db-130">Active Directory Domain Services 中的訊息</span><span class="sxs-lookup"><span data-stu-id="e07db-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





