---
title: 'WM_ADSPROP_NOTIFY_ERROR 訊息 (Adsprop .h) '
description: WM \_ ADSPROP \_ 通知 \_ 錯誤訊息會將錯誤訊息加入至透過呼叫 ADsPropShowErrorDialog 函式所顯示的錯誤訊息清單。
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103793"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="6c505-104">WM \_ ADSPROP \_ 通知 \_ 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6c505-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="6c505-105">**WM \_ ADSPROP \_ 通知 \_ 錯誤** 訊息會將錯誤訊息加入至透過呼叫 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)函式所顯示的錯誤訊息清單。</span><span class="sxs-lookup"><span data-stu-id="6c505-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="6c505-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c505-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c505-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="6c505-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6c505-108">通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c505-108">Handle of the notification object.</span></span> <span data-ttu-id="6c505-109">這是 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)所取得的 *hNotifyObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="6c505-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="6c505-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c505-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c505-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="6c505-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c505-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c505-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c505-113">[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)結構的指標，其中包含錯誤訊息資料。</span><span class="sxs-lookup"><span data-stu-id="6c505-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c505-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c505-114">Return value</span></span>

<span data-ttu-id="6c505-115">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c505-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c505-116">備註</span><span class="sxs-lookup"><span data-stu-id="6c505-116">Remarks</span></span>

<span data-ttu-id="6c505-117">[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)函數是傳送此訊息的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="6c505-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="6c505-118">在呼叫 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)之前，會累積由 **WM \_ ADSPROP \_ 通知 \_ 錯誤** 訊息所新增的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6c505-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="6c505-119">**ADsPropShowErrorDialog** 會結合並顯示累積的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6c505-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="6c505-120">當錯誤對話方塊關閉時，會刪除累積的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6c505-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c505-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c505-121">Requirements</span></span>



| <span data-ttu-id="6c505-122">需求</span><span class="sxs-lookup"><span data-stu-id="6c505-122">Requirement</span></span> | <span data-ttu-id="6c505-123">值</span><span class="sxs-lookup"><span data-stu-id="6c505-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c505-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c505-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c505-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c505-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="6c505-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c505-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c505-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c505-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="6c505-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6c505-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c505-129"><dt>Adsprop。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c505-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c505-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c505-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c505-131">Active Directory Domain Services 中的訊息</span><span class="sxs-lookup"><span data-stu-id="6c505-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="6c505-132">**ADSPROPERROR**</span><span class="sxs-lookup"><span data-stu-id="6c505-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="6c505-133">**ADsPropSendErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="6c505-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="6c505-134">**ADsPropShowErrorDialog**</span><span class="sxs-lookup"><span data-stu-id="6c505-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





