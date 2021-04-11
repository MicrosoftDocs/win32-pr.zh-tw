---
title: 'EM_SETOPTIONS 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的選項。
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094440"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="fd01c-104">EM \_ >setoptions 訊息</span><span class="sxs-lookup"><span data-stu-id="fd01c-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="fd01c-105">設定 rich edit 控制項的選項。</span><span class="sxs-lookup"><span data-stu-id="fd01c-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd01c-106">參數</span><span class="sxs-lookup"><span data-stu-id="fd01c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd01c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd01c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd01c-108">指定作業，這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fd01c-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="fd01c-109">值</span><span class="sxs-lookup"><span data-stu-id="fd01c-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="fd01c-110">意義</span><span class="sxs-lookup"><span data-stu-id="fd01c-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="fd01c-111"><dt>**ECOOP \_ 集**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="fd01c-112">將選項設定為 *lParam* 所指定的選項。</span><span class="sxs-lookup"><span data-stu-id="fd01c-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="fd01c-113"><dt>**ECOOP \_ 或**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="fd01c-114">結合指定的選項與目前的選項。</span><span class="sxs-lookup"><span data-stu-id="fd01c-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="fd01c-115"><dt>**ECOOP \_ 和**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="fd01c-116">只保留 *lParam* 中也會指定的目前選項。</span><span class="sxs-lookup"><span data-stu-id="fd01c-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="fd01c-117"><dt>**ECOOP \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="fd01c-118">以邏輯方式獨佔或目前的選項與 *lParam* 指定的選項。</span><span class="sxs-lookup"><span data-stu-id="fd01c-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd01c-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd01c-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd01c-120">指定下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="fd01c-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="fd01c-121">值</span><span class="sxs-lookup"><span data-stu-id="fd01c-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="fd01c-122">意義</span><span class="sxs-lookup"><span data-stu-id="fd01c-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="fd01c-123"><dt>**ECO \_ AUTOWORDSELECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="fd01c-124">按兩下時自動選取單字。</span><span class="sxs-lookup"><span data-stu-id="fd01c-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="fd01c-125"><dt>**ECO \_ AUTOVSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="fd01c-126">與 [**ES \_ AUTOVSCROLL**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="fd01c-127"><dt>**ECO \_ AUTOHSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="fd01c-128">與 [**ES \_ AUTOHSCROLL**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="fd01c-129"><dt>**ECO \_ NOHIDESEL**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="fd01c-130">與 [**ES \_ NOHIDESEL**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="fd01c-131"><dt>**ECO \_ READONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="fd01c-132">與 [**ES \_ READONLY**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="fd01c-133"><dt>**ECO \_ WANTRETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="fd01c-134">與 [**ES \_ WANTRETURN**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="fd01c-135"><dt>**ECO \_ SELECTIONBAR**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="fd01c-136">與 [**ES \_ SELECTIONBAR**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="fd01c-137"><dt>**經濟 \_ 垂直**</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="fd01c-138">與 [**ES \_ 垂直**](rich-edit-control-styles.md) 樣式相同。</span><span class="sxs-lookup"><span data-stu-id="fd01c-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="fd01c-139">僅適用于亞洲語言版本。</span><span class="sxs-lookup"><span data-stu-id="fd01c-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd01c-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd01c-140">Return value</span></span>

<span data-ttu-id="fd01c-141">此訊息會傳回編輯控制項的目前選項。</span><span class="sxs-lookup"><span data-stu-id="fd01c-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd01c-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd01c-142">Requirements</span></span>



| <span data-ttu-id="fd01c-143">需求</span><span class="sxs-lookup"><span data-stu-id="fd01c-143">Requirement</span></span> | <span data-ttu-id="fd01c-144">值</span><span class="sxs-lookup"><span data-stu-id="fd01c-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd01c-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd01c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fd01c-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd01c-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd01c-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd01c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fd01c-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd01c-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd01c-149">標頭</span><span class="sxs-lookup"><span data-stu-id="fd01c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd01c-150"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd01c-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd01c-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd01c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd01c-152">**Rich Edit 控制項樣式**</span><span class="sxs-lookup"><span data-stu-id="fd01c-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





