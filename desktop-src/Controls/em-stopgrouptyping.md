---
title: 'EM_STOPGROUPTYPING 訊息 (Richedit .h) '
description: 停止 rich edit 控制項，使其無法將其他輸入動作收集到目前的復原動作。 控制項會將下一個輸入動作（如果有的話）儲存至復原佇列中的新動作。
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING message Windows 控制項
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685841"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="7993b-105">EM \_ STOPGROUPTYPING 訊息</span><span class="sxs-lookup"><span data-stu-id="7993b-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="7993b-106">停止 rich edit 控制項，使其無法將其他輸入動作收集到目前的復原動作。</span><span class="sxs-lookup"><span data-stu-id="7993b-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="7993b-107">控制項會將下一個輸入動作（如果有的話）儲存至復原佇列中的新動作。</span><span class="sxs-lookup"><span data-stu-id="7993b-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="7993b-108">參數</span><span class="sxs-lookup"><span data-stu-id="7993b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7993b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7993b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7993b-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="7993b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7993b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7993b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7993b-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="7993b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7993b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7993b-113">Return value</span></span>

<span data-ttu-id="7993b-114">傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="7993b-114">The return value is zero.</span></span> <span data-ttu-id="7993b-115">此訊息無法失敗。</span><span class="sxs-lookup"><span data-stu-id="7993b-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="7993b-116">備註</span><span class="sxs-lookup"><span data-stu-id="7993b-116">Remarks</span></span>

<span data-ttu-id="7993b-117">Rich edit 控制項會將連續的輸入動作（包括使用 **倒退鍵** 刪除的字元）分組成單一復原動作，直到發生下列其中一個事件為止：</span><span class="sxs-lookup"><span data-stu-id="7993b-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="7993b-118">控制項收到 **EM \_ STOPGROUPTYPING** 訊息。</span><span class="sxs-lookup"><span data-stu-id="7993b-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="7993b-119">控制項失去焦點。</span><span class="sxs-lookup"><span data-stu-id="7993b-119">The control loses focus.</span></span>
-   <span data-ttu-id="7993b-120">使用者可以使用方向鍵或按一下滑鼠來移動目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="7993b-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="7993b-121">使用者按下 **Delete** 鍵。</span><span class="sxs-lookup"><span data-stu-id="7993b-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="7993b-122">使用者執行任何其他動作，例如 **不包含輸入** 的貼上作業。</span><span class="sxs-lookup"><span data-stu-id="7993b-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="7993b-123">您可以傳送 **EM \_ STOPGROUPTYPING** 訊息，將連續的輸入動作分成較小的復原群組。</span><span class="sxs-lookup"><span data-stu-id="7993b-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="7993b-124">例如，您可以在每個字元之後或每個斷字字元之後傳送 **EM \_ STOPGROUPTYPING** 。</span><span class="sxs-lookup"><span data-stu-id="7993b-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="7993b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7993b-125">Requirements</span></span>



| <span data-ttu-id="7993b-126">需求</span><span class="sxs-lookup"><span data-stu-id="7993b-126">Requirement</span></span> | <span data-ttu-id="7993b-127">值</span><span class="sxs-lookup"><span data-stu-id="7993b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7993b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7993b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7993b-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7993b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7993b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7993b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7993b-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7993b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7993b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7993b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7993b-133"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7993b-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7993b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7993b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7993b-135">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="7993b-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





