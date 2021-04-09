---
title: 'EM_SETLIMITTEXT 訊息 (Winuser .h) '
description: 設定編輯控制項的文字限制。
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686034"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="74c9b-104">EM \_ SETLIMITTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="74c9b-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="74c9b-105">設定編輯控制項的文字限制。</span><span class="sxs-lookup"><span data-stu-id="74c9b-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="74c9b-106">文字限制是使用者可以在編輯控制項中輸入的最大文字數量（以 **TCHAR** s 為限）。</span><span class="sxs-lookup"><span data-stu-id="74c9b-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="74c9b-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="74c9b-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="74c9b-108">若為編輯控制項和 Microsoft Rich Edit 1.0，則會使用 bytes。</span><span class="sxs-lookup"><span data-stu-id="74c9b-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="74c9b-109">針對 Microsoft Rich Edit 2.0 和更新版本，會使用字元。</span><span class="sxs-lookup"><span data-stu-id="74c9b-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="74c9b-110">**Em \_ SETLIMITTEXT** 訊息等同于 [**em \_ LIMITTEXT**](em-limittext.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="74c9b-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="74c9b-111">參數</span><span class="sxs-lookup"><span data-stu-id="74c9b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c9b-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74c9b-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74c9b-113">使用者可以輸入的最大 **TCHAR** 數。</span><span class="sxs-lookup"><span data-stu-id="74c9b-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="74c9b-114">若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。</span><span class="sxs-lookup"><span data-stu-id="74c9b-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="74c9b-115">此數目不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="74c9b-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="74c9b-116">**Rich edit 控制項：** 如果此參數為零，則文字長度會設定為64000個字元。</span><span class="sxs-lookup"><span data-stu-id="74c9b-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="74c9b-117">如果此參數為零，則文字長度會設為單行編輯控制項的0x7FFFFFFE 字元，或1表示多行編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="74c9b-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="74c9b-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74c9b-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74c9b-119">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="74c9b-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c9b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="74c9b-120">Return value</span></span>

<span data-ttu-id="74c9b-121">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="74c9b-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c9b-122">備註</span><span class="sxs-lookup"><span data-stu-id="74c9b-122">Remarks</span></span>

<span data-ttu-id="74c9b-123">**EM \_ SETLIMITTEXT** 訊息只會限制使用者可以輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="74c9b-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="74c9b-124">當傳送訊息時，它不會影響任何已在編輯控制項中的文字，也不會影響由 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息複製到編輯控制項的文字長度。</span><span class="sxs-lookup"><span data-stu-id="74c9b-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="74c9b-125">如果應用程式使用 **WM \_ SETTEXT** 訊息將更多文字放入編輯控制項中，而不是在 **EM \_ SETLIMITTEXT** 訊息中指定，則使用者可以編輯編輯控制項的整個內容。</span><span class="sxs-lookup"><span data-stu-id="74c9b-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="74c9b-126">在呼叫 **EM \_ SETLIMITTEXT** 之前，使用者可以在編輯控制項中輸入的文字數量預設限制為32767個字元。</span><span class="sxs-lookup"><span data-stu-id="74c9b-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="74c9b-127">針對單行編輯控制項，文字限制為0x7FFFFFFE 個位元組或 *wParam* 參數的值，以較小者為准。</span><span class="sxs-lookup"><span data-stu-id="74c9b-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="74c9b-128">若為多行編輯控制項，此值為1個位元組或 *wParam* 參數的值，以較小者為准。</span><span class="sxs-lookup"><span data-stu-id="74c9b-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="74c9b-129">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="74c9b-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="74c9b-130">使用 message [**EM \_ EXLIMITTEXT**](em-exlimittext.md) 來取得大於64000的文字長度值。</span><span class="sxs-lookup"><span data-stu-id="74c9b-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="74c9b-131">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="74c9b-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74c9b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="74c9b-132">Requirements</span></span>



| <span data-ttu-id="74c9b-133">需求</span><span class="sxs-lookup"><span data-stu-id="74c9b-133">Requirement</span></span> | <span data-ttu-id="74c9b-134">值</span><span class="sxs-lookup"><span data-stu-id="74c9b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c9b-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74c9b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="74c9b-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c9b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74c9b-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74c9b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="74c9b-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c9b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74c9b-139">標頭</span><span class="sxs-lookup"><span data-stu-id="74c9b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="74c9b-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="74c9b-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74c9b-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74c9b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c9b-142">**EM \_ GETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="74c9b-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

