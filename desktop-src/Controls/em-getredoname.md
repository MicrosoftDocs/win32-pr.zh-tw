---
title: 'EM_GETREDONAME 訊息 (Richedit .h) '
description: 在 rich edit 控制項的重做佇列中，抓取下一個動作的型別（如果有的話）。
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934488"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="4a696-104">EM \_ GETREDONAME 訊息</span><span class="sxs-lookup"><span data-stu-id="4a696-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="4a696-105">在 rich edit 控制項的重做佇列中，抓取下一個動作的型別（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="4a696-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a696-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a696-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a696-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a696-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a696-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="4a696-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a696-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a696-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a696-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="4a696-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a696-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a696-111">Return value</span></span>

<span data-ttu-id="4a696-112">如果控制項的重做佇列不是空的，則傳回的值會是 [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) 列舉值，指出控制項的重做佇列中下一個動作的類型。</span><span class="sxs-lookup"><span data-stu-id="4a696-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="4a696-113">如果沒有 redoable 的動作，或下一個 redoable 動作的型別未知，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="4a696-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a696-114">備註</span><span class="sxs-lookup"><span data-stu-id="4a696-114">Remarks</span></span>

<span data-ttu-id="4a696-115">可以復原或重做的動作類型包括輸入、刪除、拖放、剪下和貼上作業。</span><span class="sxs-lookup"><span data-stu-id="4a696-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="4a696-116">這項資訊適用于提供復原和重做作業之擴充使用者介面的應用程式，例如 redoable 動作的下拉式清單方塊。</span><span class="sxs-lookup"><span data-stu-id="4a696-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a696-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a696-117">Requirements</span></span>



| <span data-ttu-id="4a696-118">需求</span><span class="sxs-lookup"><span data-stu-id="4a696-118">Requirement</span></span> | <span data-ttu-id="4a696-119">值</span><span class="sxs-lookup"><span data-stu-id="4a696-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a696-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a696-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a696-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a696-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a696-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a696-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a696-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a696-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a696-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4a696-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a696-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a696-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a696-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a696-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a696-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="4a696-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a696-128">**EM \_ GETUNDONAME**</span><span class="sxs-lookup"><span data-stu-id="4a696-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="4a696-129">**EM \_ 重做**</span><span class="sxs-lookup"><span data-stu-id="4a696-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="4a696-130">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="4a696-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="4a696-131">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="4a696-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





