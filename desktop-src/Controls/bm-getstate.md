---
title: 'BM_GETSTATE 訊息 (Winuser .h) '
description: 抓取按鈕或核取方塊的狀態。 您可以明確地傳送此訊息，或使用按鈕 \_ >getstate 宏。
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933969"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="8a288-105">BM \_ >getstate 訊息</span><span class="sxs-lookup"><span data-stu-id="8a288-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="8a288-106">抓取按鈕或核取方塊的狀態。</span><span class="sxs-lookup"><span data-stu-id="8a288-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="8a288-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ >getstate**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="8a288-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a288-108">參數</span><span class="sxs-lookup"><span data-stu-id="8a288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a288-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a288-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a288-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="8a288-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8a288-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a288-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a288-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="8a288-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a288-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a288-113">Return value</span></span>

<span data-ttu-id="8a288-114">傳回值會指定按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8a288-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="8a288-115">它是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="8a288-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="8a288-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8a288-116">Return code</span></span>                                                                                        | <span data-ttu-id="8a288-117">Description</span><span class="sxs-lookup"><span data-stu-id="8a288-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a288-118"><dt>**BST \_ 已核取**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="8a288-119">按鈕已核取。</span><span class="sxs-lookup"><span data-stu-id="8a288-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="8a288-120"><dt>**BST \_ DROPDOWNPUSHED**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="8a288-121">[Windows Vista](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="8a288-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="8a288-122">按鈕處於下拉式狀態。</span><span class="sxs-lookup"><span data-stu-id="8a288-122">The button is in the drop-down state.</span></span> <span data-ttu-id="8a288-123">僅適用于按鈕具有 [ [**TBSTYLE \_ ] 下拉式**](toolbar-control-and-button-styles.md) 樣式時。</span><span class="sxs-lookup"><span data-stu-id="8a288-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="8a288-124"><dt>**BST \_ 焦點**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="8a288-125">按鈕具有鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="8a288-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="8a288-126"><dt>**BST \_ 熱**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="8a288-127">按鈕是經常性的;也就是滑鼠停留在其上方。</span><span class="sxs-lookup"><span data-stu-id="8a288-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="8a288-128"><dt>**BST \_ 不定**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="8a288-129">按鈕的狀態為不定。</span><span class="sxs-lookup"><span data-stu-id="8a288-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="8a288-130">只有在按鈕具有 [**BS \_ 3STATE**](button-styles.md) 或 [**BS \_ AUTO3STATE**](button-styles.md) 樣式時才適用。</span><span class="sxs-lookup"><span data-stu-id="8a288-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="8a288-131"><dt>**BST \_ 推送**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="8a288-132">此按鈕會顯示為已推送的狀態。</span><span class="sxs-lookup"><span data-stu-id="8a288-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="8a288-133"><dt>**未核取 BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8a288-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="8a288-134">沒有特殊狀態。</span><span class="sxs-lookup"><span data-stu-id="8a288-134">No special state.</span></span> <span data-ttu-id="8a288-135">相當於零。</span><span class="sxs-lookup"><span data-stu-id="8a288-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8a288-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a288-136">Requirements</span></span>



| <span data-ttu-id="8a288-137">需求</span><span class="sxs-lookup"><span data-stu-id="8a288-137">Requirement</span></span> | <span data-ttu-id="8a288-138">值</span><span class="sxs-lookup"><span data-stu-id="8a288-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a288-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a288-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8a288-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a288-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8a288-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a288-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8a288-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a288-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8a288-143">標頭</span><span class="sxs-lookup"><span data-stu-id="8a288-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a288-144"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8a288-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a288-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a288-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a288-146">**參考**</span><span class="sxs-lookup"><span data-stu-id="8a288-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8a288-147">**BM \_ GETCHECK**</span><span class="sxs-lookup"><span data-stu-id="8a288-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="8a288-148">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="8a288-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





