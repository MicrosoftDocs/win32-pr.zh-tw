---
title: 'EM_SETIMEMODEBIAS 訊息 (Richedit .h) '
description: 針對 rich edit 控制項設定輸入法的 (IME) 模式偏差。
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465709"
---
# <a name="em_setimemodebias-message"></a><span data-ttu-id="f4fd8-104">EM \_ SETIMEMODEBIAS 訊息</span><span class="sxs-lookup"><span data-stu-id="f4fd8-104">EM\_SETIMEMODEBIAS message</span></span>

<span data-ttu-id="f4fd8-105">針對 rich edit 控制項設定輸入法的 (IME) 模式偏差。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-105">Set the Input Method Editor (IME) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4fd8-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4fd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4fd8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4fd8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fd8-108">輸入法模式偏差值。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-108">IME mode bias value.</span></span> <span data-ttu-id="f4fd8-109">它可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-109">It can be one of the following.</span></span>



| <span data-ttu-id="f4fd8-110">值</span><span class="sxs-lookup"><span data-stu-id="f4fd8-110">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="f4fd8-111">意義</span><span class="sxs-lookup"><span data-stu-id="f4fd8-111">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <span data-ttu-id="f4fd8-112"><dt>**IMF \_ SMODE \_ PLAURALCLAUSE**</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd8-112"><dt>**IMF\_SMODE\_PLAURALCLAUSE**</dt></span></span> </dl> | <span data-ttu-id="f4fd8-113">將輸入法模式偏差設定為 Name。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-113">Sets the IME mode bias to Name.</span></span><br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <span data-ttu-id="f4fd8-114"><dt>**IMF \_ SMODE \_ NONE**</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd8-114"><dt>**IMF\_SMODE\_NONE**</dt></span></span> </dl>                            | <span data-ttu-id="f4fd8-115">無偏差。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-115">No bias.</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="f4fd8-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4fd8-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4fd8-117">這必須與 *wParam* 的值相同。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-117">This must be the same value as *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4fd8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4fd8-118">Return value</span></span>

<span data-ttu-id="f4fd8-119">此訊息會傳回新的 IME 模式偏差設定。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-119">This message returns the new IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4fd8-120">備註</span><span class="sxs-lookup"><span data-stu-id="f4fd8-120">Remarks</span></span>

<span data-ttu-id="f4fd8-121">當 IME 產生一組字元的替代挑選清單時，此訊息會設定一些選項會出現在清單頂端的準則。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-121">When the IME generates a list of alternative choices for a set of characters, this message sets the criteria by which some of the choices will appear at the top of the list.</span></span>

<span data-ttu-id="f4fd8-122">若要將文字服務架構 (TSF) 模式偏差，請使用 [**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-122">To set the Text Services Framework (TSF) mode bias, use [**EM\_SETCTFMODEBIAS**](em-setctfmodebias.md).</span></span>

<span data-ttu-id="f4fd8-123">在呼叫此函式之前，應用程式應該呼叫 [**EM \_ ISIME**](em-isime.md) 。</span><span class="sxs-lookup"><span data-stu-id="f4fd8-123">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fd8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4fd8-124">Requirements</span></span>



| <span data-ttu-id="f4fd8-125">需求</span><span class="sxs-lookup"><span data-stu-id="f4fd8-125">Requirement</span></span> | <span data-ttu-id="f4fd8-126">值</span><span class="sxs-lookup"><span data-stu-id="f4fd8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fd8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4fd8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fd8-128">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4fd8-128">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4fd8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4fd8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fd8-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4fd8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4fd8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f4fd8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4fd8-132"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd8-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fd8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4fd8-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4fd8-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="f4fd8-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4fd8-135">**EM \_ ISIME**</span><span class="sxs-lookup"><span data-stu-id="f4fd8-135">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="f4fd8-136">**EM \_ SETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="f4fd8-136">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> </dl>

 

 





