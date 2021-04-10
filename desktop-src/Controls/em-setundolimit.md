---
title: 'EM_SETUNDOLIMIT 訊息 (Richedit .h) '
description: 設定可在 rich edit 控制項的復原佇列中儲存的動作數目上限。
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934540"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="4d8bf-104">EM \_ SETUNDOLIMIT 訊息</span><span class="sxs-lookup"><span data-stu-id="4d8bf-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="4d8bf-105">設定可在 rich edit 控制項的復原佇列中儲存的動作數目上限。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d8bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d8bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d8bf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8bf-108">指定可儲存在復原佇列中的動作數目上限。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="4d8bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d8bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8bf-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8bf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d8bf-111">Return value</span></span>

<span data-ttu-id="4d8bf-112">傳回值是 rich edit 控制項的新復原動作最大數目。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="4d8bf-113">如果記憶體有限，則這個值可能小於 *wParam* 。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d8bf-114">備註</span><span class="sxs-lookup"><span data-stu-id="4d8bf-114">Remarks</span></span>

<span data-ttu-id="4d8bf-115">根據預設，復原佇列中的動作數目上限為100。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="4d8bf-116">如果您增加此數目，則必須有足夠的可用記憶體來容納新的數位。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="4d8bf-117">為了達到較佳的效能，請將限制設定為最小的可能值。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="4d8bf-118">將 [限制] 設定為 [零] 會停用 **復原** 功能。</span><span class="sxs-lookup"><span data-stu-id="4d8bf-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8bf-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d8bf-119">Requirements</span></span>



| <span data-ttu-id="4d8bf-120">需求</span><span class="sxs-lookup"><span data-stu-id="4d8bf-120">Requirement</span></span> | <span data-ttu-id="4d8bf-121">值</span><span class="sxs-lookup"><span data-stu-id="4d8bf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8bf-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d8bf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8bf-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d8bf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d8bf-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d8bf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8bf-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d8bf-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d8bf-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4d8bf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d8bf-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d8bf-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8bf-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d8bf-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d8bf-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="4d8bf-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4d8bf-130">**EM \_ CANREDO**</span><span class="sxs-lookup"><span data-stu-id="4d8bf-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="4d8bf-131">**EM \_ GETREDONAME**</span><span class="sxs-lookup"><span data-stu-id="4d8bf-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="4d8bf-132">**EM \_ GETUNDONAME**</span><span class="sxs-lookup"><span data-stu-id="4d8bf-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="4d8bf-133">**EM \_ 重做**</span><span class="sxs-lookup"><span data-stu-id="4d8bf-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="4d8bf-134">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="4d8bf-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





