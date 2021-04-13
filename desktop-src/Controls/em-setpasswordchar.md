---
title: 'EM_SETPASSWORDCHAR 訊息 (Winuser .h) '
description: 設定或移除編輯控制項的密碼字元。 設定密碼字元時，會顯示該字元來取代使用者輸入的字元。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465053"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="ec7f9-106">EM \_ SETPASSWORDCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="ec7f9-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="ec7f9-107">設定或移除編輯控制項的密碼字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="ec7f9-108">設定密碼字元時，會顯示該字元來取代使用者輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="ec7f9-109">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec7f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec7f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec7f9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec7f9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7f9-112">要顯示的字元，用來取代使用者輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="ec7f9-113">如果此參數為零，控制項會移除目前的密碼字元，並顯示使用者輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="ec7f9-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec7f9-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7f9-115">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec7f9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec7f9-116">Return value</span></span>

<span data-ttu-id="ec7f9-117">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7f9-118">備註</span><span class="sxs-lookup"><span data-stu-id="ec7f9-118">Remarks</span></span>

<span data-ttu-id="ec7f9-119">當編輯控制項收到 **EM \_ SETPASSWORDCHAR** 訊息時，控制項會使用 *wParam* 參數指定的字元來重繪所有可見字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="ec7f9-120">如果 *wParam* 為零，控制項會使用使用者輸入的字元來重繪所有可見字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="ec7f9-121">如果以 [**ES \_ 密碼**](edit-control-styles.md) 樣式建立編輯控制項，則預設密碼字元會設定為星號 (\*) 。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="ec7f9-122">如果建立不含 **ES \_ 密碼** 樣式的編輯控制項，則不會有密碼字元。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="ec7f9-123">如果 **EM \_ SETPASSWORDCHAR** 訊息是以 *wParam* 參數設定為零，則會移除 **ES \_ 密碼** 樣式。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="ec7f9-124">**編輯控制項：** 多行編輯控制項不支援密碼樣式或訊息。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="ec7f9-125">**Rich Edit：** Microsoft Rich Edit 2.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="ec7f9-126">單行和多行編輯控制項都支援密碼樣式和訊息。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="ec7f9-127">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="ec7f9-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7f9-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec7f9-128">Requirements</span></span>



| <span data-ttu-id="ec7f9-129">需求</span><span class="sxs-lookup"><span data-stu-id="ec7f9-129">Requirement</span></span> | <span data-ttu-id="ec7f9-130">值</span><span class="sxs-lookup"><span data-stu-id="ec7f9-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7f9-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec7f9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7f9-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec7f9-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec7f9-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec7f9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7f9-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec7f9-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec7f9-135">標頭</span><span class="sxs-lookup"><span data-stu-id="ec7f9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec7f9-136"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ec7f9-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7f9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec7f9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7f9-138">**EM \_ GETPASSWORDCHAR**</span><span class="sxs-lookup"><span data-stu-id="ec7f9-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 





