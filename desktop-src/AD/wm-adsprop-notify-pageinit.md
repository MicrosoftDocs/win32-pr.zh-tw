---
title: 'WM_ADSPROP_NOTIFY_PAGEINIT 訊息 (Adsprop .h) '
description: Active Directory 屬性工作表延伸模組會呼叫 ADsPropGetInitInfo，以取得有關屬性工作表延伸適用之目錄物件的相關資料。
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508456"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="050bb-104">WM \_ ADSPROP \_ 通知 \_ PAGEINIT 訊息</span><span class="sxs-lookup"><span data-stu-id="050bb-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="050bb-105">Active Directory 屬性工作表延伸模組會呼叫 [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) ，以取得有關屬性工作表延伸適用之目錄物件的相關資料。</span><span class="sxs-lookup"><span data-stu-id="050bb-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="050bb-106">**ADsPropGetInitInfo** 函式會將 **WM \_ ADSPROP \_ 通知 \_ PAGEINIT** 訊息傳送至通知物件，以達成此結果。</span><span class="sxs-lookup"><span data-stu-id="050bb-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="050bb-107">參數</span><span class="sxs-lookup"><span data-stu-id="050bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="050bb-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="050bb-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="050bb-109">通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="050bb-109">Handle of the notification object.</span></span> <span data-ttu-id="050bb-110">這是呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)所取得的 *hNotifyObject* 參數。</span><span class="sxs-lookup"><span data-stu-id="050bb-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="050bb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="050bb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="050bb-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="050bb-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="050bb-113">*pADsPropInitParams*</span><span class="sxs-lookup"><span data-stu-id="050bb-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="050bb-114">接收目錄物件資訊之 [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="050bb-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="050bb-115">這是傳遞至 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)的 *pInitParams* 參數。</span><span class="sxs-lookup"><span data-stu-id="050bb-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="050bb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="050bb-116">Return value</span></span>

<span data-ttu-id="050bb-117">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="050bb-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="050bb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="050bb-118">Requirements</span></span>



| <span data-ttu-id="050bb-119">需求</span><span class="sxs-lookup"><span data-stu-id="050bb-119">Requirement</span></span> | <span data-ttu-id="050bb-120">值</span><span class="sxs-lookup"><span data-stu-id="050bb-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="050bb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="050bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="050bb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="050bb-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="050bb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="050bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="050bb-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="050bb-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="050bb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="050bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="050bb-126"><dt>Adsprop。h</dt></span><span class="sxs-lookup"><span data-stu-id="050bb-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050bb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="050bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050bb-128">Active Directory Domain Services 中的訊息</span><span class="sxs-lookup"><span data-stu-id="050bb-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="050bb-129">**ADsPropGetInitInfo**</span><span class="sxs-lookup"><span data-stu-id="050bb-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="050bb-130">**ADSPROPINITPARAMS**</span><span class="sxs-lookup"><span data-stu-id="050bb-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





