---
title: 'WM_ADSPROP_NOTIFY_PAGEHWND 訊息 (Adsprop .h) '
description: Active Directory Directory 服務屬性工作表延伸模組會呼叫 ADsPropSetHwnd，以通知屬性頁面視窗控制碼的通知物件。
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105617"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="d2b73-104">WM \_ ADSPROP \_ 通知 \_ PAGEHWND 訊息</span><span class="sxs-lookup"><span data-stu-id="d2b73-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="d2b73-105">Active Directory Directory 服務屬性工作表延伸模組會呼叫 [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) ，以通知屬性頁面視窗控制碼的通知物件。</span><span class="sxs-lookup"><span data-stu-id="d2b73-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="d2b73-106">**ADsPropSetHwnd** 函式會將 **WM \_ ADSPROP \_ 通知 \_ PAGEHWND** 訊息傳送至通知物件，此物件會通知屬性頁面視窗控制碼的通知物件。</span><span class="sxs-lookup"><span data-stu-id="d2b73-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="d2b73-107">參數</span><span class="sxs-lookup"><span data-stu-id="d2b73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b73-108">*hNotifyObj*</span><span class="sxs-lookup"><span data-stu-id="d2b73-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b73-109">通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2b73-109">The handle of the notification object.</span></span> <span data-ttu-id="d2b73-110">若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。</span><span class="sxs-lookup"><span data-stu-id="d2b73-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="d2b73-111">*hPage*</span><span class="sxs-lookup"><span data-stu-id="d2b73-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b73-112">屬性頁的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2b73-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="d2b73-113">*ptzTitle*</span><span class="sxs-lookup"><span data-stu-id="d2b73-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b73-114">以 Null 終止的 **WCHAR** 緩衝區指標，其中包含屬性頁的標題。</span><span class="sxs-lookup"><span data-stu-id="d2b73-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b73-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2b73-115">Return value</span></span>

<span data-ttu-id="d2b73-116">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="d2b73-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2b73-117">備註</span><span class="sxs-lookup"><span data-stu-id="d2b73-117">Remarks</span></span>

<span data-ttu-id="d2b73-118">Active Directory 的屬性工作表延伸模組通常會在處理 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)訊息時呼叫 [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)函數。</span><span class="sxs-lookup"><span data-stu-id="d2b73-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b73-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2b73-119">Requirements</span></span>



| <span data-ttu-id="d2b73-120">需求</span><span class="sxs-lookup"><span data-stu-id="d2b73-120">Requirement</span></span> | <span data-ttu-id="d2b73-121">值</span><span class="sxs-lookup"><span data-stu-id="d2b73-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b73-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2b73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b73-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2b73-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="d2b73-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2b73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b73-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2b73-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="d2b73-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d2b73-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2b73-127"><dt>Adsprop。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b73-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b73-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2b73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b73-129">Active Directory Domain Services 中的訊息</span><span class="sxs-lookup"><span data-stu-id="d2b73-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="d2b73-130">**ADsPropSetHwnd**</span><span class="sxs-lookup"><span data-stu-id="d2b73-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="d2b73-131">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="d2b73-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="d2b73-132">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="d2b73-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

