---
title: 'EM_GETIMESTATUS 訊息 (Winuser .h) '
description: 取得一組狀態旗標，指出編輯控制項如何與輸入方法編輯器互動 (IME) 。
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105120"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="bf38c-104">EM \_ GETIMESTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="bf38c-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="bf38c-105">取得一組狀態旗標，指出編輯控制項如何與輸入方法編輯器互動 (IME) 。</span><span class="sxs-lookup"><span data-stu-id="bf38c-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="bf38c-106">參數</span><span class="sxs-lookup"><span data-stu-id="bf38c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf38c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf38c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf38c-108">要取出的狀態類型。</span><span class="sxs-lookup"><span data-stu-id="bf38c-108">The type of status to retrieve.</span></span> <span data-ttu-id="bf38c-109">此參數可為下列值。</span><span class="sxs-lookup"><span data-stu-id="bf38c-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="bf38c-110">值</span><span class="sxs-lookup"><span data-stu-id="bf38c-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="bf38c-111">意義</span><span class="sxs-lookup"><span data-stu-id="bf38c-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="bf38c-112"><dt>**EMSIS \_ COMPOSITIONSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="bf38c-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="bf38c-113">設定處理組合字元串的行為。</span><span class="sxs-lookup"><span data-stu-id="bf38c-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf38c-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf38c-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf38c-115">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="bf38c-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf38c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf38c-116">Return value</span></span>

<span data-ttu-id="bf38c-117">要抓取之狀態類型的特定資料。</span><span class="sxs-lookup"><span data-stu-id="bf38c-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="bf38c-118">針對 *status* 的 **EMSIS \_ COMPOSITIONSTRING** 值，此傳回值是下列其中一個或多個值。</span><span class="sxs-lookup"><span data-stu-id="bf38c-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="bf38c-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bf38c-119">Return code</span></span>                                                                                                    | <span data-ttu-id="bf38c-120">Description</span><span class="sxs-lookup"><span data-stu-id="bf38c-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf38c-121"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="bf38c-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="bf38c-122">如果設定此旗標，則編輯控制項會將 *fFlags* 設定為 gc RESULTSTR 的 [**WM \_ IME \_ 組合**](/windows/desktop/Intl/wm-ime-composition)訊息進行攔截， \_ 並立即傳回結果字串。</span><span class="sxs-lookup"><span data-stu-id="bf38c-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="bf38c-123">如果未設定此旗標，則編輯控制項會將 **wm \_ IME \_ 組合** 訊息傳遞至預設視窗程式，並處理來自 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息的結果字串，這是編輯控制項的預設行為。</span><span class="sxs-lookup"><span data-stu-id="bf38c-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="bf38c-124"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="bf38c-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="bf38c-125">如果設定此旗標，則編輯控制項會在收到 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息時取消撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="bf38c-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="bf38c-126">如果未設定此旗標，則編輯控制項不會取消撰寫字串;這是編輯控制項的預設行為。</span><span class="sxs-lookup"><span data-stu-id="bf38c-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="bf38c-127"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="bf38c-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="bf38c-128">如果設定此旗標，則編輯控制項會在收到 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) 訊息時完成組合字元串。</span><span class="sxs-lookup"><span data-stu-id="bf38c-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="bf38c-129">如果未設定此旗標，則編輯控制項不會完成組合字元串;這是編輯控制項的預設行為。</span><span class="sxs-lookup"><span data-stu-id="bf38c-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="bf38c-130">備註</span><span class="sxs-lookup"><span data-stu-id="bf38c-130">Remarks</span></span>

<span data-ttu-id="bf38c-131">**Rich Edit：** 不支援 **EM \_ GETIMESTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="bf38c-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf38c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf38c-132">Requirements</span></span>



| <span data-ttu-id="bf38c-133">需求</span><span class="sxs-lookup"><span data-stu-id="bf38c-133">Requirement</span></span> | <span data-ttu-id="bf38c-134">值</span><span class="sxs-lookup"><span data-stu-id="bf38c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf38c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf38c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf38c-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf38c-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bf38c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf38c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf38c-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf38c-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bf38c-139">標頭</span><span class="sxs-lookup"><span data-stu-id="bf38c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf38c-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bf38c-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf38c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf38c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf38c-142">**EM \_ SETIMESTATUS**</span><span class="sxs-lookup"><span data-stu-id="bf38c-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

