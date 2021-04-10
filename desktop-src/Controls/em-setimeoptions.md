---
title: 'EM_SETIMEOPTIONS 訊息 (Richedit .h) '
description: 將輸入方法編輯器 (IME) 選項。
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843811"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="84060-104">EM \_ SETIMEOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="84060-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="84060-105">將輸入方法編輯器 (IME) 選項。</span><span class="sxs-lookup"><span data-stu-id="84060-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="84060-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="84060-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="84060-107">任何較新版本都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="84060-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="84060-108">參數</span><span class="sxs-lookup"><span data-stu-id="84060-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84060-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84060-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84060-110">指定下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="84060-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="84060-111">值</span><span class="sxs-lookup"><span data-stu-id="84060-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="84060-112">意義</span><span class="sxs-lookup"><span data-stu-id="84060-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="84060-113"><dt>**ECOOP \_ 集**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="84060-114">將選項設定為 *lParam* 所指定的選項。</span><span class="sxs-lookup"><span data-stu-id="84060-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="84060-115"><dt>**ECOOP \_ 或**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="84060-116">結合指定的選項與目前的選項。</span><span class="sxs-lookup"><span data-stu-id="84060-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="84060-117"><dt>**ECOOP \_ 和**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="84060-118">只保留 *lParam* 中也會指定的目前選項。</span><span class="sxs-lookup"><span data-stu-id="84060-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="84060-119"><dt>**ECOOP \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="84060-120">以邏輯方式獨佔或目前的選項與 LParam 指定的選項 *。*</span><span class="sxs-lookup"><span data-stu-id="84060-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84060-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84060-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84060-122">指定下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="84060-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="84060-123">值</span><span class="sxs-lookup"><span data-stu-id="84060-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="84060-124">意義</span><span class="sxs-lookup"><span data-stu-id="84060-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="84060-125"><dt>**IMF \_ CLOSESTATUSWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="84060-126">當控制項收到輸入焦點時，關閉輸入法狀態視窗。</span><span class="sxs-lookup"><span data-stu-id="84060-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="84060-127"><dt>**IMF \_ FORCEACTIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="84060-128">當控制項收到輸入焦點時啟用 IME。</span><span class="sxs-lookup"><span data-stu-id="84060-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="84060-129"><dt>**IMF \_ FORCEDISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="84060-130">當控制項收到輸入焦點時，停用 IME。</span><span class="sxs-lookup"><span data-stu-id="84060-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="84060-131"><dt>**IMF \_ FORCEENABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="84060-132">當控制項收到輸入焦點時啟用 IME。</span><span class="sxs-lookup"><span data-stu-id="84060-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="84060-133"><dt>**IMF \_ FORCEINACTIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="84060-134">當控制項收到輸入焦點時，會 IME。</span><span class="sxs-lookup"><span data-stu-id="84060-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="84060-135"><dt>**IMF \_ FORCENONE**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="84060-136">停用 IME 處理。</span><span class="sxs-lookup"><span data-stu-id="84060-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="84060-137"><dt>**IMF \_ FORCEREMEMBER**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="84060-138">當控制項收到輸入焦點時，還原先前的輸入法狀態。</span><span class="sxs-lookup"><span data-stu-id="84060-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="84060-139"><dt>**IMF \_ MULTIPLEEDIT**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="84060-140">指定將不會取消或決定焦點變更的組合字元串。</span><span class="sxs-lookup"><span data-stu-id="84060-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="84060-141">這可讓應用程式在每個 rich edit 控制項上都有個別的組合字元串。</span><span class="sxs-lookup"><span data-stu-id="84060-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="84060-142"><dt>**IMF \_ 垂直**</dt></span><span class="sxs-lookup"><span data-stu-id="84060-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="84060-143">請注意，在豐富的編輯2.0 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="84060-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84060-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="84060-144">Return value</span></span>

<span data-ttu-id="84060-145">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="84060-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="84060-146">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="84060-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="84060-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="84060-147">Requirements</span></span>



| <span data-ttu-id="84060-148">需求</span><span class="sxs-lookup"><span data-stu-id="84060-148">Requirement</span></span> | <span data-ttu-id="84060-149">值</span><span class="sxs-lookup"><span data-stu-id="84060-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84060-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84060-150">Minimum supported client</span></span><br/> | <span data-ttu-id="84060-151">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84060-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84060-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84060-152">Minimum supported server</span></span><br/> | <span data-ttu-id="84060-153">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84060-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84060-154">標頭</span><span class="sxs-lookup"><span data-stu-id="84060-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="84060-155"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="84060-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84060-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84060-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84060-157">**EM \_ GETIMEOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="84060-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





