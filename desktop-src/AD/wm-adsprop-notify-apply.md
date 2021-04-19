---
title: 'WM_ADSPROP_NOTIFY_APPLY 訊息 (Adsprop .h) '
description: '\_ \_ \_ 如果屬性頁 PSN 套用 \_ 處理常式成功，則 Active Directory Directory 服務屬性工作表延伸會將 WM ADSPROP 通知套用訊息傳送至通知物件。'
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967560"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="e42a5-104">WM \_ ADSPROP \_ 通知套用 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="e42a5-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="e42a5-105">如果屬性頁 PSN 套用處理程式成功，則 Active Directory Directory 服務屬性工作表延伸會將 **WM \_ ADSPROP \_ 通知 \_** 套用訊息傳送至通知物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e42a5-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="e42a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="e42a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42a5-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="e42a5-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e42a5-108">通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e42a5-108">The handle of the notification object.</span></span> <span data-ttu-id="e42a5-109">若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。</span><span class="sxs-lookup"><span data-stu-id="e42a5-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="e42a5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e42a5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e42a5-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="e42a5-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e42a5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e42a5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e42a5-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="e42a5-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42a5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e42a5-114">Return value</span></span>

<span data-ttu-id="e42a5-115">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e42a5-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e42a5-116">備註</span><span class="sxs-lookup"><span data-stu-id="e42a5-116">Remarks</span></span>

<span data-ttu-id="e42a5-117">將頁面新增至 Active Directory Manager MMC 嵌入式管理單元時，Active Directory MMC 屬性工作表會透過呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) 函式來建立通知物件，然後將通知物件控制碼傳遞至每個屬性頁。</span><span class="sxs-lookup"><span data-stu-id="e42a5-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="e42a5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e42a5-118">Requirements</span></span>



| <span data-ttu-id="e42a5-119">需求</span><span class="sxs-lookup"><span data-stu-id="e42a5-119">Requirement</span></span> | <span data-ttu-id="e42a5-120">值</span><span class="sxs-lookup"><span data-stu-id="e42a5-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e42a5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e42a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e42a5-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e42a5-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="e42a5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e42a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e42a5-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e42a5-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="e42a5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e42a5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e42a5-126"><dt>Adsprop。h</dt></span><span class="sxs-lookup"><span data-stu-id="e42a5-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e42a5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e42a5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42a5-128">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="e42a5-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="e42a5-129">Active Directory Domain Services 中的訊息</span><span class="sxs-lookup"><span data-stu-id="e42a5-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





