---
title: 'EM_SETLANGOPTIONS 訊息 (Richedit .h) '
description: 在 rich edit 控制項中設定輸入方法編輯器 (IME) 和亞洲語言支援的選項。
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934274"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="ba2c0-104">EM \_ SETLANGOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="ba2c0-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="ba2c0-105">在 rich edit 控制項中設定輸入方法編輯器 (IME) 和亞洲語言支援的選項。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba2c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ba2c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba2c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba2c0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba2c0-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba2c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba2c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba2c0-110">指定語言選項。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-110">Specifies the language options.</span></span> <span data-ttu-id="ba2c0-111">如需可能值的清單，請參閱 [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba2c0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba2c0-112">Return value</span></span>

<span data-ttu-id="ba2c0-113">此訊息會傳回值1。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba2c0-114">備註</span><span class="sxs-lookup"><span data-stu-id="ba2c0-114">Remarks</span></span>

<span data-ttu-id="ba2c0-115">**EM \_ SETLANGOPTIONS** 訊息會控制下列各項：</span><span class="sxs-lookup"><span data-stu-id="ba2c0-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="ba2c0-116">自動字型系結。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-116">Automatic font binding.</span></span>
-   <span data-ttu-id="ba2c0-117">自動切換鍵盤。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="ba2c0-118">自動調整字型大小大小。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="ba2c0-119">使用使用者介面預設字型，而不是檔預設字型。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="ba2c0-120">在 IME 組合期間對用戶端的通知。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="ba2c0-121">IME 如何中止組合模式。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="ba2c0-122">拼寫檢查、自動校正和觸控鍵盤預測。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="ba2c0-123">這則訊息會設定所有語言選項旗標的值。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="ba2c0-124">若要變更旗標的子集，請傳送 [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md) 訊息以取得目前的選項旗標、變更您需要變更的旗標，然後傳送 **EM \_ SETLANGOPTIONS** 訊息與結果。</span><span class="sxs-lookup"><span data-stu-id="ba2c0-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba2c0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba2c0-125">Requirements</span></span>



| <span data-ttu-id="ba2c0-126">需求</span><span class="sxs-lookup"><span data-stu-id="ba2c0-126">Requirement</span></span> | <span data-ttu-id="ba2c0-127">值</span><span class="sxs-lookup"><span data-stu-id="ba2c0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba2c0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba2c0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba2c0-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba2c0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba2c0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba2c0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba2c0-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba2c0-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba2c0-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ba2c0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba2c0-133"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba2c0-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba2c0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba2c0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba2c0-135">**EM \_ GETLANGOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="ba2c0-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





