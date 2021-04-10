---
title: 'EM_CANREDO 訊息 (Richedit .h) '
description: 判斷控制項重做佇列中是否有任何動作。
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- EM_CANREDO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843896"
---
# <a name="em_canredo-message"></a><span data-ttu-id="5d4c2-104">EM \_ CANREDO 訊息</span><span class="sxs-lookup"><span data-stu-id="5d4c2-104">EM\_CANREDO message</span></span>

<span data-ttu-id="5d4c2-105">判斷控制項重做佇列中是否有任何動作。</span><span class="sxs-lookup"><span data-stu-id="5d4c2-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d4c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="5d4c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d4c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d4c2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d4c2-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d4c2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d4c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d4c2-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d4c2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d4c2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d4c2-111">Return value</span></span>

<span data-ttu-id="5d4c2-112">如果控制項重做佇列中有動作，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="5d4c2-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="5d4c2-113">如果重做佇列是空的，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5d4c2-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4c2-114">備註</span><span class="sxs-lookup"><span data-stu-id="5d4c2-114">Remarks</span></span>

<span data-ttu-id="5d4c2-115">若要取消復原最近的復原作業，請傳送 [**EM \_ 重做**](em-redo.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="5d4c2-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4c2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d4c2-116">Requirements</span></span>



| <span data-ttu-id="5d4c2-117">需求</span><span class="sxs-lookup"><span data-stu-id="5d4c2-117">Requirement</span></span> | <span data-ttu-id="5d4c2-118">值</span><span class="sxs-lookup"><span data-stu-id="5d4c2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4c2-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d4c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5d4c2-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d4c2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d4c2-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d4c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5d4c2-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d4c2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d4c2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5d4c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d4c2-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4c2-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d4c2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d4c2-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d4c2-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="5d4c2-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d4c2-127">**EM \_ GETREDONAME**</span><span class="sxs-lookup"><span data-stu-id="5d4c2-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="5d4c2-128">**EM \_ GETUNDONAME**</span><span class="sxs-lookup"><span data-stu-id="5d4c2-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="5d4c2-129">**EM \_ 重做**</span><span class="sxs-lookup"><span data-stu-id="5d4c2-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="5d4c2-130">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="5d4c2-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





