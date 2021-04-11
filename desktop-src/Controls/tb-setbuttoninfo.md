---
title: 'TB_SETBUTTONINFO 訊息 (Commctrl .h) '
description: 設定工具列中現有按鈕的資訊。
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844263"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="c6b6e-104">TB \_ SETBUTTONINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="c6b6e-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="c6b6e-105">設定工具列中現有按鈕的資訊。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6b6e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6b6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b6e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6b6e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b6e-108">按鈕識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c6b6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6b6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b6e-110">[**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)結構的指標，其中包含新的按鈕資訊。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="c6b6e-111">在傳送此訊息之前，必須先填入此結構的 **cbSize** 和 **dwMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6b6e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6b6e-112">Return value</span></span>

<span data-ttu-id="c6b6e-113">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b6e-114">備註</span><span class="sxs-lookup"><span data-stu-id="c6b6e-114">Remarks</span></span>

<span data-ttu-id="c6b6e-115">將文字新增至工具列時，通常會將文字指派給按鈕，方法是在工具列的字串集區中指定字串的索引。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="c6b6e-116">如果您使用 **TB \_ SETBUTTONINFO** 將新文字指派給按鈕，則會從字串集區永久覆寫文字。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="c6b6e-117">您可以再次呼叫 **TB \_ SETBUTTONINFO** 來變更文字，但無法從字串集區重新指派字串。</span><span class="sxs-lookup"><span data-stu-id="c6b6e-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b6e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6b6e-118">Requirements</span></span>



| <span data-ttu-id="c6b6e-119">需求</span><span class="sxs-lookup"><span data-stu-id="c6b6e-119">Requirement</span></span> | <span data-ttu-id="c6b6e-120">值</span><span class="sxs-lookup"><span data-stu-id="c6b6e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b6e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6b6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b6e-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6b6e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6b6e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6b6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b6e-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6b6e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6b6e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c6b6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b6e-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b6e-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c6b6e-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c6b6e-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c6b6e-128">**TB \_SETBUTTONINFOW** (Unicode) 和 **TB \_ SETBUTTONINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c6b6e-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c6b6e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6b6e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6b6e-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6b6e-131">**TB \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="c6b6e-132">**TB \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="c6b6e-133">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="c6b6e-134">**TB \_ GETSTRING**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="c6b6e-135">**TB \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="c6b6e-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





