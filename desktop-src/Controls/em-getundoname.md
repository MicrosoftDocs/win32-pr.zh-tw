---
title: 'EM_GETUNDONAME 訊息 (Richedit .h) '
description: Microsoft Rich Edit 2.0 和更新版本會捕獲下一個復原動作的類型（如果有的話）。Microsoft Rich Edit 1.0 不支援此訊息。
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934808"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="be513-104">EM \_ GETUNDONAME 訊息</span><span class="sxs-lookup"><span data-stu-id="be513-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="be513-105">Microsoft Rich Edit 2.0 和更新版本：抓取下一個復原動作的型別（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="be513-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="be513-106">Microsoft Rich Edit 1.0：不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="be513-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="be513-107">參數</span><span class="sxs-lookup"><span data-stu-id="be513-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be513-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be513-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be513-109">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="be513-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="be513-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be513-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be513-111">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="be513-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be513-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="be513-112">Return value</span></span>

<span data-ttu-id="be513-113">如果有復原動作，傳回的值會是 [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) 列舉值，指出控制項復原佇列中下一個動作的類型。</span><span class="sxs-lookup"><span data-stu-id="be513-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="be513-114">如果沒有可復原的動作，或下一個復原動作的類型未知，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="be513-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="be513-115">備註</span><span class="sxs-lookup"><span data-stu-id="be513-115">Remarks</span></span>

<span data-ttu-id="be513-116">可以復原或重做的動作類型包括輸入、刪除、拖放、卸載、剪下和貼上作業。</span><span class="sxs-lookup"><span data-stu-id="be513-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="be513-117">這項資訊對於提供復原和重做作業擴充使用者介面的應用程式很有用，例如可復原之動作的下拉式清單方塊。</span><span class="sxs-lookup"><span data-stu-id="be513-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="be513-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="be513-118">Requirements</span></span>



| <span data-ttu-id="be513-119">需求</span><span class="sxs-lookup"><span data-stu-id="be513-119">Requirement</span></span> | <span data-ttu-id="be513-120">值</span><span class="sxs-lookup"><span data-stu-id="be513-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be513-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be513-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be513-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be513-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be513-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be513-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be513-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be513-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be513-125">標頭</span><span class="sxs-lookup"><span data-stu-id="be513-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be513-126"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="be513-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be513-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be513-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="be513-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="be513-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be513-129">**EM \_ GETREDONAME**</span><span class="sxs-lookup"><span data-stu-id="be513-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="be513-130">**EM \_ 重做**</span><span class="sxs-lookup"><span data-stu-id="be513-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="be513-131">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="be513-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="be513-132">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="be513-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





