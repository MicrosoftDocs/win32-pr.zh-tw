---
title: 'EM_SETIMESTATUS 訊息 (Winuser .h) '
description: 設定狀態旗標，以決定編輯控制項如何與輸入方法編輯器互動 (IME) 。
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686035"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="1a264-104">EM \_ SETIMESTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="1a264-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="1a264-105">設定狀態旗標，以決定編輯控制項如何與輸入方法編輯器互動 (IME) 。</span><span class="sxs-lookup"><span data-stu-id="1a264-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="1a264-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a264-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a264-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a264-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a264-108">要設定的狀態類型。</span><span class="sxs-lookup"><span data-stu-id="1a264-108">The type of status to set.</span></span> <span data-ttu-id="1a264-109">此參數可為下列值。</span><span class="sxs-lookup"><span data-stu-id="1a264-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="1a264-110">值</span><span class="sxs-lookup"><span data-stu-id="1a264-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="1a264-111">意義</span><span class="sxs-lookup"><span data-stu-id="1a264-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="1a264-112"><dt>**EMSIS \_ COMPOSITIONSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="1a264-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="1a264-113">設定處理撰寫字串的行為。</span><span class="sxs-lookup"><span data-stu-id="1a264-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1a264-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a264-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a264-115">狀態類型的特定資料。</span><span class="sxs-lookup"><span data-stu-id="1a264-115">Data specific to the status type.</span></span> <span data-ttu-id="1a264-116">如果 *wParam* 是 **EMSIS \_ COMPOSITIONSTRING**，則這個參數可以是下列其中一個或多個值。</span><span class="sxs-lookup"><span data-stu-id="1a264-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1a264-117">值</span><span class="sxs-lookup"><span data-stu-id="1a264-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="1a264-118">意義</span><span class="sxs-lookup"><span data-stu-id="1a264-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="1a264-119"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="1a264-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="1a264-120">如果設定此旗標，則編輯控制項會將 *lParam* 設定為 gc RESULTSTR 的 [**WM \_ IME \_ 組合**](/windows/desktop/Intl/wm-ime-composition)訊息進行攔截， \_ 並立即傳回結果字串。</span><span class="sxs-lookup"><span data-stu-id="1a264-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="1a264-121">如果未設定此旗標，則編輯控制項會將 **wm \_ IME \_ 組合** 訊息傳遞至預設視窗程式，並處理來自 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息的結果字串，這是編輯控制項的預設行為。</span><span class="sxs-lookup"><span data-stu-id="1a264-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="1a264-122"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="1a264-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="1a264-123">如果設定此旗標，則編輯控制項會在收到 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息時取消撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="1a264-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="1a264-124">如果未設定此旗標，則編輯控制項不會取消撰寫字串;這是編輯控制項的預設行為。</span><span class="sxs-lookup"><span data-stu-id="1a264-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="1a264-125"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="1a264-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="1a264-126">如果設定此旗標，則編輯控制項會在收到 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) 訊息時完成組合字元串。</span><span class="sxs-lookup"><span data-stu-id="1a264-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="1a264-127">如果未設定此旗標，則編輯控制項不會完成組合字元串;這是編輯控制項的預設行為。</span><span class="sxs-lookup"><span data-stu-id="1a264-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a264-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a264-128">Return value</span></span>

<span data-ttu-id="1a264-129">傳回 *lParam* 參數的先前值。</span><span class="sxs-lookup"><span data-stu-id="1a264-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a264-130">備註</span><span class="sxs-lookup"><span data-stu-id="1a264-130">Remarks</span></span>

<span data-ttu-id="1a264-131">**Rich Edit：** 不支援 **EM \_ SETIMESTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1a264-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a264-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a264-132">Requirements</span></span>



| <span data-ttu-id="1a264-133">需求</span><span class="sxs-lookup"><span data-stu-id="1a264-133">Requirement</span></span> | <span data-ttu-id="1a264-134">值</span><span class="sxs-lookup"><span data-stu-id="1a264-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a264-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a264-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1a264-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a264-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a264-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a264-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1a264-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a264-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a264-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1a264-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a264-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1a264-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a264-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a264-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a264-142">**EM \_ GETIMESTATUS**</span><span class="sxs-lookup"><span data-stu-id="1a264-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

