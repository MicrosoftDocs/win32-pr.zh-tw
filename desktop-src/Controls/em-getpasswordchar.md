---
title: 'EM_GETPASSWORDCHAR 訊息 (Winuser .h) '
description: 取得當使用者輸入文字時，編輯控制項所顯示的密碼字元。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844135"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="03edd-105">EM \_ GETPASSWORDCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="03edd-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="03edd-106">取得當使用者輸入文字時，編輯控制項所顯示的密碼字元。</span><span class="sxs-lookup"><span data-stu-id="03edd-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="03edd-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="03edd-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="03edd-108">參數</span><span class="sxs-lookup"><span data-stu-id="03edd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03edd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03edd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03edd-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="03edd-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="03edd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03edd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03edd-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="03edd-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03edd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="03edd-113">Return value</span></span>

<span data-ttu-id="03edd-114">傳回值會指定要顯示的字元，以取代使用者輸入的任何字元。</span><span class="sxs-lookup"><span data-stu-id="03edd-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="03edd-115">如果傳回值為 **Null**，則不會有密碼字元，而且控制項會顯示使用者輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="03edd-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="03edd-116">備註</span><span class="sxs-lookup"><span data-stu-id="03edd-116">Remarks</span></span>

<span data-ttu-id="03edd-117">如果以 [**ES \_ 密碼**](edit-control-styles.md) 樣式建立編輯控制項，則預設密碼字元會設定為星號 (\*) 。</span><span class="sxs-lookup"><span data-stu-id="03edd-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="03edd-118">如果建立不含 **ES \_ 密碼** 樣式的編輯控制項，則不會有密碼字元。</span><span class="sxs-lookup"><span data-stu-id="03edd-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="03edd-119">若要變更密碼字元，請傳送 [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="03edd-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="03edd-120">**編輯控制項：** 多行編輯控制項不支援密碼樣式或訊息。</span><span class="sxs-lookup"><span data-stu-id="03edd-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="03edd-121">**Rich edit：** Microsoft Rich Edit 2.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="03edd-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="03edd-122">單行和多行編輯控制項都支援密碼樣式和訊息。</span><span class="sxs-lookup"><span data-stu-id="03edd-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="03edd-123">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="03edd-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03edd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="03edd-124">Requirements</span></span>



| <span data-ttu-id="03edd-125">需求</span><span class="sxs-lookup"><span data-stu-id="03edd-125">Requirement</span></span> | <span data-ttu-id="03edd-126">值</span><span class="sxs-lookup"><span data-stu-id="03edd-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03edd-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03edd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="03edd-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03edd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03edd-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03edd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="03edd-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03edd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03edd-131">標頭</span><span class="sxs-lookup"><span data-stu-id="03edd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="03edd-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="03edd-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03edd-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03edd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03edd-134">**EM \_ SETPASSWORDCHAR**</span><span class="sxs-lookup"><span data-stu-id="03edd-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 





