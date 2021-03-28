---
description: 表示顯示快顯功能表時可用的選項。
title: 'MP_POPUPFLAGS 常數 (Shobjidl.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113968"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="0e67c-103">MP \_ POPUPFLAGS 常數</span><span class="sxs-lookup"><span data-stu-id="0e67c-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="0e67c-104">表示顯示快顯功能表時可用的選項。</span><span class="sxs-lookup"><span data-stu-id="0e67c-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="0e67c-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="0e67c-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="0e67c-106">Description</span><span class="sxs-lookup"><span data-stu-id="0e67c-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="0e67c-107"><dt>**MPPF \_SETFOCUS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="0e67c-108">提供快顯功能表焦點。</span><span class="sxs-lookup"><span data-stu-id="0e67c-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="0e67c-109"><dt>**MPPF \_INITIALSELECT**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="0e67c-110">選取快顯功能表中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="0e67c-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="0e67c-111"><dt>**MPPF \_NOANIMATE**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="0e67c-112">在顯示功能表時，請勿使用預設的系統動畫，例如淡入。</span><span class="sxs-lookup"><span data-stu-id="0e67c-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="0e67c-113"><dt>**MPPF \_鍵盤**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="0e67c-114">依鍵盤快速鍵啟動功能表。</span><span class="sxs-lookup"><span data-stu-id="0e67c-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="0e67c-115"><dt>**MPPF \_重新置放**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="0e67c-116">根據功能表的變更，將列顯示在不同的位置。</span><span class="sxs-lookup"><span data-stu-id="0e67c-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="0e67c-117"><dt>**MPPF \_FORCEZORDER**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="0e67c-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="0e67c-118">Reserved.</span></span> <span data-ttu-id="0e67c-119">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="0e67c-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="0e67c-120"><dt>**MPPF \_FINALSELECT**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="0e67c-121">選取功能表中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="0e67c-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="0e67c-122"><dt>**MPPF \_靠 \_ 左對齊**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="0e67c-123">**Windows Vista 或更新版本**：在 [**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)或 [**IMenuPopup：:P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)的 *prcExclude* 參數中指定的區域左邊對齊快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="0e67c-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="0e67c-124">這是預設的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="0e67c-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="0e67c-125"><dt>**MPPF \_靠 \_ 右對齊**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="0e67c-126">**Windows Vista 或更新版本**：在 [**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)或 [**IMenuPopup：:P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)的 *prcExclude* 參數中指定的區域右邊對齊快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="0e67c-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="0e67c-127"><dt>**MPPF \_TOP**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="0e67c-128">將快顯功能表放在 [**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)或 [**IMenuPopup：:P**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)之 *ppt* 參數所指定的初始點上方。</span><span class="sxs-lookup"><span data-stu-id="0e67c-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="0e67c-129"><dt>**MPPF \_左方**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="0e67c-130">將快顯功能表放在初始點的左邊。</span><span class="sxs-lookup"><span data-stu-id="0e67c-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="0e67c-131"><dt>**MPPF \_RIGHT**</dt> <dt>0x60000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="0e67c-132">將快顯功能表放在初始點的右邊。</span><span class="sxs-lookup"><span data-stu-id="0e67c-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="0e67c-133"><dt>**MPPF \_底部**</dt> <dt> (int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="0e67c-134">將快顯功能表放在初始點下方。</span><span class="sxs-lookup"><span data-stu-id="0e67c-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="0e67c-135"><dt>**MPPF \_POS \_ 遮罩**</dt> <dt> (int) 0xE0000000</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="0e67c-136">功能表位置遮罩。</span><span class="sxs-lookup"><span data-stu-id="0e67c-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="0e67c-137">備註</span><span class="sxs-lookup"><span data-stu-id="0e67c-137">Remarks</span></span>

<span data-ttu-id="0e67c-138">這些常數定義于從 Windows XP Service Pack 1 (SP1) 和 Windows Server 2003 開始的 Shobjidl.h .h 檔案</span><span class="sxs-lookup"><span data-stu-id="0e67c-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="0e67c-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e67c-139">Requirements</span></span>



| <span data-ttu-id="0e67c-140">需求</span><span class="sxs-lookup"><span data-stu-id="0e67c-140">Requirement</span></span> | <span data-ttu-id="0e67c-141">值</span><span class="sxs-lookup"><span data-stu-id="0e67c-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e67c-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e67c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0e67c-143">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e67c-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e67c-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e67c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0e67c-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e67c-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e67c-146">標頭</span><span class="sxs-lookup"><span data-stu-id="0e67c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e67c-147"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e67c-148">Idl</span><span class="sxs-lookup"><span data-stu-id="0e67c-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0e67c-149"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0e67c-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e67c-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e67c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e67c-151">**IMenuPopup：:P opup**</span><span class="sxs-lookup"><span data-stu-id="0e67c-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="0e67c-152">**ITrackShellMenu：:P opup**</span><span class="sxs-lookup"><span data-stu-id="0e67c-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




