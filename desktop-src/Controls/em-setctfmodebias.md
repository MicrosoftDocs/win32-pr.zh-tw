---
title: 'EM_SETCTFMODEBIAS 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的文字服務架構 (TSF) 模式偏差。
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509172"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="36527-104">EM \_ SETCTFMODEBIAS 訊息</span><span class="sxs-lookup"><span data-stu-id="36527-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="36527-105">設定 rich edit 控制項的文字服務架構 (TSF) 模式偏差。</span><span class="sxs-lookup"><span data-stu-id="36527-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="36527-106">參數</span><span class="sxs-lookup"><span data-stu-id="36527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36527-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36527-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36527-108">模式偏差值。</span><span class="sxs-lookup"><span data-stu-id="36527-108">Mode bias value.</span></span> <span data-ttu-id="36527-109">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36527-109">This can be one of the following values.</span></span>



| <span data-ttu-id="36527-110">值</span><span class="sxs-lookup"><span data-stu-id="36527-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="36527-111">意義</span><span class="sxs-lookup"><span data-stu-id="36527-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="36527-112"><dt>**CTFMODEBIAS \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="36527-113">沒有模式偏差。</span><span class="sxs-lookup"><span data-stu-id="36527-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="36527-114"><dt>**CTFMODEBIAS \_ 檔案名**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="36527-115">偏差是檔案名。</span><span class="sxs-lookup"><span data-stu-id="36527-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="36527-116"><dt>**CTFMODEBIAS \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="36527-117">偏差是指名稱。</span><span class="sxs-lookup"><span data-stu-id="36527-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="36527-118"><dt>**CTFMODEBIAS \_ 閱讀**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="36527-119">偏差是讀取的。</span><span class="sxs-lookup"><span data-stu-id="36527-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="36527-120"><dt>**CTFMODEBIAS \_ DATETIME**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="36527-121">偏差是指日期或時間。</span><span class="sxs-lookup"><span data-stu-id="36527-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="36527-122"><dt>**CTFMODEBIAS \_ 對話**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="36527-123">偏差是指交談。</span><span class="sxs-lookup"><span data-stu-id="36527-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="36527-124"><dt>**CTFMODEBIAS \_ 數值**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="36527-125">偏差是數位。</span><span class="sxs-lookup"><span data-stu-id="36527-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="36527-126"><dt>**CTFMODEBIAS \_ 平假名**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="36527-127">偏差是指平假名字串。</span><span class="sxs-lookup"><span data-stu-id="36527-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="36527-128"><dt>**CTFMODEBIAS \_ 片假名**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="36527-129">偏差是片假名字串。</span><span class="sxs-lookup"><span data-stu-id="36527-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="36527-130"><dt>**CTFMODEBIAS \_ 韓文**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="36527-131">偏差是以韓文字元為單位。</span><span class="sxs-lookup"><span data-stu-id="36527-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="36527-132"><dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="36527-133">偏差是半形片假名字串。</span><span class="sxs-lookup"><span data-stu-id="36527-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="36527-134"><dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="36527-135">偏差是全形的英數位元。</span><span class="sxs-lookup"><span data-stu-id="36527-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="36527-136"><dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="36527-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="36527-137">偏差是半形的英數位元。</span><span class="sxs-lookup"><span data-stu-id="36527-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36527-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36527-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36527-139">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="36527-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36527-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="36527-140">Return value</span></span>

<span data-ttu-id="36527-141">如果成功，傳回值就是新的 TSF 模式偏差值。</span><span class="sxs-lookup"><span data-stu-id="36527-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="36527-142">如果不成功，則傳回值為舊的 TSF 模式偏差值。</span><span class="sxs-lookup"><span data-stu-id="36527-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36527-143">備註</span><span class="sxs-lookup"><span data-stu-id="36527-143">Remarks</span></span>

<span data-ttu-id="36527-144">當 Microsoft Rich Edit 應用程式使用 TSF 時，可以選取 TSF 模式偏差。</span><span class="sxs-lookup"><span data-stu-id="36527-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="36527-145">這則訊息會設定在清單頂端顯示替代選項的準則，以供選取。</span><span class="sxs-lookup"><span data-stu-id="36527-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="36527-146">若要為輸入方法編輯器設定模式偏差 (IME) ，請使用 [**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)。</span><span class="sxs-lookup"><span data-stu-id="36527-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36527-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="36527-147">Requirements</span></span>



| <span data-ttu-id="36527-148">需求</span><span class="sxs-lookup"><span data-stu-id="36527-148">Requirement</span></span> | <span data-ttu-id="36527-149">值</span><span class="sxs-lookup"><span data-stu-id="36527-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36527-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36527-150">Minimum supported client</span></span><br/> | <span data-ttu-id="36527-151">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36527-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36527-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36527-152">Minimum supported server</span></span><br/> | <span data-ttu-id="36527-153">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36527-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36527-154">標頭</span><span class="sxs-lookup"><span data-stu-id="36527-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="36527-155"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="36527-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36527-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36527-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="36527-157">**參考**</span><span class="sxs-lookup"><span data-stu-id="36527-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36527-158">**EM \_ GETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="36527-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="36527-159">**EM \_ SETIMEMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="36527-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





