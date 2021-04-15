---
title: 'EM_TAKEFOCUS 訊息 (Commctrl .h) '
description: 強制單行編輯控制項接收鍵盤焦點。 您可以使用 [編輯 TakeFocus] 宏明確地傳送此訊息 \_ 。
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465381"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="ec653-105">EM \_ TAKEFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="ec653-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="ec653-106">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="ec653-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="ec653-107">未來的 Windows 版本可能不支援此訊息。\]</span><span class="sxs-lookup"><span data-stu-id="ec653-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="ec653-108">強制單行編輯控制項接收鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="ec653-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="ec653-109">您可以使用 [ [**編輯 \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) ] 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ec653-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec653-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec653-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec653-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec653-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec653-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="ec653-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec653-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec653-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec653-114">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="ec653-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec653-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec653-115">Return value</span></span>

<span data-ttu-id="ec653-116">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec653-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="ec653-117">安全性考量</span><span class="sxs-lookup"><span data-stu-id="ec653-117">Security Considerations</span></span>

<span data-ttu-id="ec653-118">使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="ec653-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec653-119">備註</span><span class="sxs-lookup"><span data-stu-id="ec653-119">Remarks</span></span>

<span data-ttu-id="ec653-120">如果編輯控制項不是單行編輯控制項，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="ec653-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="ec653-121">如果編輯控制項先前收到 [**EM \_ NOSETFOCUS**](em-nosetfocus.md) 訊息，則編輯控制項將會顯示焦點，而不會實際擁有焦點; 否則，編輯控制項將會獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="ec653-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec653-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec653-122">Requirements</span></span>



| <span data-ttu-id="ec653-123">需求</span><span class="sxs-lookup"><span data-stu-id="ec653-123">Requirement</span></span> | <span data-ttu-id="ec653-124">值</span><span class="sxs-lookup"><span data-stu-id="ec653-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec653-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec653-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ec653-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec653-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec653-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec653-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ec653-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec653-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec653-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ec653-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec653-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec653-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec653-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec653-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec653-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="ec653-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ec653-133">**編輯 \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="ec653-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="ec653-134">**EM \_ NOSETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="ec653-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 





