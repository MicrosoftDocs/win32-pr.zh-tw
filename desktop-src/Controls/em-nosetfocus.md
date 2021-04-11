---
title: 'EM_NOSETFOCUS 訊息 (Commctrl .h) '
description: 防止單一行編輯控制項接收鍵盤焦點。 您可以使用 [編輯 NoSetFocus] 宏明確地傳送此訊息 \_ 。
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105102"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="b70e8-105">EM \_ NOSETFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="b70e8-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="b70e8-106">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="b70e8-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="b70e8-107">未來的 Windows 版本可能不支援此訊息。\]</span><span class="sxs-lookup"><span data-stu-id="b70e8-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="b70e8-108">防止單一行編輯控制項接收鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="b70e8-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="b70e8-109">您可以使用 [ [**編輯 \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) ] 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b70e8-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b70e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="b70e8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70e8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b70e8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b70e8-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b70e8-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b70e8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b70e8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b70e8-114">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b70e8-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70e8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b70e8-115">Return value</span></span>

<span data-ttu-id="b70e8-116">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="b70e8-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="b70e8-117">安全性考量</span><span class="sxs-lookup"><span data-stu-id="b70e8-117">Security Considerations</span></span>

<span data-ttu-id="b70e8-118">使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="b70e8-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="b70e8-119">備註</span><span class="sxs-lookup"><span data-stu-id="b70e8-119">Remarks</span></span>

<span data-ttu-id="b70e8-120">如果編輯控制項不是單行編輯控制項，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="b70e8-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="b70e8-121">傳送此訊息之後，效果會是永久性的。</span><span class="sxs-lookup"><span data-stu-id="b70e8-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70e8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b70e8-122">Requirements</span></span>



| <span data-ttu-id="b70e8-123">需求</span><span class="sxs-lookup"><span data-stu-id="b70e8-123">Requirement</span></span> | <span data-ttu-id="b70e8-124">值</span><span class="sxs-lookup"><span data-stu-id="b70e8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b70e8-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b70e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b70e8-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b70e8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b70e8-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b70e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b70e8-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b70e8-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b70e8-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b70e8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b70e8-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b70e8-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b70e8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b70e8-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="b70e8-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="b70e8-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b70e8-133">**編輯 \_ NoSetFocus**</span><span class="sxs-lookup"><span data-stu-id="b70e8-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="b70e8-134">**EM \_ TAKEFOCUS**</span><span class="sxs-lookup"><span data-stu-id="b70e8-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 





