---
title: 'EM_REDO 訊息 (Richedit .h) '
description: 將 EM \_ 重做訊息傳送至 rich edit 控制項，以重做控制項的重做佇列中的下一個動作。
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO message Windows 控制項
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465897"
---
# <a name="em_redo-message"></a><span data-ttu-id="c4d54-104">EM \_ 重做訊息</span><span class="sxs-lookup"><span data-stu-id="c4d54-104">EM\_REDO message</span></span>

<span data-ttu-id="c4d54-105">將 **EM \_ 重做** 訊息傳送至 rich edit 控制項，以重做控制項的重做佇列中的下一個動作。</span><span class="sxs-lookup"><span data-stu-id="c4d54-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4d54-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4d54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4d54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4d54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4d54-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="c4d54-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4d54-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4d54-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4d54-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="c4d54-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4d54-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4d54-111">Return value</span></span>

<span data-ttu-id="c4d54-112">如果 **重做** 作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="c4d54-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c4d54-113">如果 **重做** 作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c4d54-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4d54-114">備註</span><span class="sxs-lookup"><span data-stu-id="c4d54-114">Remarks</span></span>

<span data-ttu-id="c4d54-115">若要判斷控制項的重做佇列中是否有任何動作，請傳送 [**EM \_ CANREDO**](em-canredo.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="c4d54-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d54-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4d54-116">Requirements</span></span>



| <span data-ttu-id="c4d54-117">需求</span><span class="sxs-lookup"><span data-stu-id="c4d54-117">Requirement</span></span> | <span data-ttu-id="c4d54-118">值</span><span class="sxs-lookup"><span data-stu-id="c4d54-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d54-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4d54-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d54-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4d54-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4d54-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4d54-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d54-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4d54-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4d54-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c4d54-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4d54-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4d54-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d54-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4d54-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4d54-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="c4d54-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4d54-127">**EM \_ CANREDO**</span><span class="sxs-lookup"><span data-stu-id="c4d54-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="c4d54-128">**EM \_ GETREDONAME**</span><span class="sxs-lookup"><span data-stu-id="c4d54-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="c4d54-129">**EM \_ GETUNDONAME**</span><span class="sxs-lookup"><span data-stu-id="c4d54-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="c4d54-130">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="c4d54-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





