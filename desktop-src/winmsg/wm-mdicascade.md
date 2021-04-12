---
description: 應用程式會將 WM \_ MDICASCADE 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以串聯格式排列其所有子視窗。
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: 'WM_MDICASCADE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318256"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="d81a8-103">WM \_ MDICASCADE 訊息</span><span class="sxs-lookup"><span data-stu-id="d81a8-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="d81a8-104">應用程式會將 **WM \_ MDICASCADE** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以串聯格式排列其所有子視窗。</span><span class="sxs-lookup"><span data-stu-id="d81a8-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="d81a8-105">參數</span><span class="sxs-lookup"><span data-stu-id="d81a8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81a8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d81a8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d81a8-107">重疊顯示行為。</span><span class="sxs-lookup"><span data-stu-id="d81a8-107">The cascade behavior.</span></span> <span data-ttu-id="d81a8-108">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="d81a8-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="d81a8-109">值</span><span class="sxs-lookup"><span data-stu-id="d81a8-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="d81a8-110">意義</span><span class="sxs-lookup"><span data-stu-id="d81a8-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="d81a8-111"><dt>**MDITILE \_SKIPDISABLED**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="d81a8-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="d81a8-112">防止停用的 MDI 子視窗進行串聯。</span><span class="sxs-lookup"><span data-stu-id="d81a8-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="d81a8-113"><dt>**MDITILE \_ZORDER**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="d81a8-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="d81a8-114">以 Z 順序排列視窗。</span><span class="sxs-lookup"><span data-stu-id="d81a8-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="d81a8-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d81a8-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d81a8-116">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d81a8-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81a8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d81a8-117">Return value</span></span>

<span data-ttu-id="d81a8-118">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="d81a8-118">Type: **BOOL**</span></span>

<span data-ttu-id="d81a8-119">如果訊息成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d81a8-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="d81a8-120">如果訊息失敗，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d81a8-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81a8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d81a8-121">Requirements</span></span>



| <span data-ttu-id="d81a8-122">需求</span><span class="sxs-lookup"><span data-stu-id="d81a8-122">Requirement</span></span> | <span data-ttu-id="d81a8-123">值</span><span class="sxs-lookup"><span data-stu-id="d81a8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81a8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d81a8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d81a8-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d81a8-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d81a8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d81a8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d81a8-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d81a8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d81a8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d81a8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d81a8-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d81a8-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d81a8-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d81a8-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="d81a8-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="d81a8-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d81a8-132">**WM \_ MDIICONARRANGE**</span><span class="sxs-lookup"><span data-stu-id="d81a8-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="d81a8-133">**WM \_ MDITILE**</span><span class="sxs-lookup"><span data-stu-id="d81a8-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="d81a8-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="d81a8-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d81a8-135">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="d81a8-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




