---
title: POPUPMENUITEM 結構
description: 包含功能表資源中開啟功能表或子功能表的功能表項目相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- POPUPMENUITEM 結構功能表和其他資源
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934050"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="70ea9-105">POPUPMENUITEM 結構</span><span class="sxs-lookup"><span data-stu-id="70ea9-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="70ea9-106">包含功能表資源中開啟功能表或子功能表的功能表項目相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70ea9-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="70ea9-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="70ea9-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ea9-108">語法</span><span class="sxs-lookup"><span data-stu-id="70ea9-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="70ea9-109">成員</span><span class="sxs-lookup"><span data-stu-id="70ea9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="70ea9-110">**type**</span><span class="sxs-lookup"><span data-stu-id="70ea9-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="70ea9-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="70ea9-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="70ea9-112">描述功能表項目。</span><span class="sxs-lookup"><span data-stu-id="70ea9-112">Describes the menu item.</span></span> <span data-ttu-id="70ea9-113">這個成員可以有的一些值包含下列清單所示的值。</span><span class="sxs-lookup"><span data-stu-id="70ea9-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="70ea9-114">除了顯示的值以外，這個成員也可以是與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構的 **fType** 成員一起列出的型別值組合。</span><span class="sxs-lookup"><span data-stu-id="70ea9-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="70ea9-115">型別值是以 MFT 開頭的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="70ea9-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="70ea9-116">若要使用這些預先定義 \_ \* 的 MFT 類型值，請在您的 .rc 檔中加入下列語句：</span><span class="sxs-lookup"><span data-stu-id="70ea9-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="70ea9-117">值</span><span class="sxs-lookup"><span data-stu-id="70ea9-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="70ea9-118">意義</span><span class="sxs-lookup"><span data-stu-id="70ea9-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="70ea9-119"><dt>**MF \_END**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="70ea9-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="70ea9-120">功能表項目是功能表上的最後一個;系統會在內部使用旗標。</span><span class="sxs-lookup"><span data-stu-id="70ea9-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="70ea9-121"><dt>**MF \_POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="70ea9-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="70ea9-122">功能表項目會開啟功能表或子功能表;系統會在內部使用旗標。</span><span class="sxs-lookup"><span data-stu-id="70ea9-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="70ea9-123">**state**</span><span class="sxs-lookup"><span data-stu-id="70ea9-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="70ea9-124">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="70ea9-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="70ea9-125">描述功能表項目。</span><span class="sxs-lookup"><span data-stu-id="70ea9-125">Describes the menu item.</span></span> <span data-ttu-id="70ea9-126">這個成員可以是與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構的 **dwState** 成員一起列出之狀態值的組合。</span><span class="sxs-lookup"><span data-stu-id="70ea9-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="70ea9-127">狀態值是以 MFS 開頭的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="70ea9-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="70ea9-128">若要使用這些預先定義 \_ \* 的 MFS 狀態值，請在 .rc 檔中加入下列語句：</span><span class="sxs-lookup"><span data-stu-id="70ea9-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="70ea9-129">**id**</span><span class="sxs-lookup"><span data-stu-id="70ea9-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="70ea9-130">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="70ea9-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="70ea9-131">識別在 [**WM \_ 命令**](wm-command.md) 訊息中傳遞之功能表項目的數值運算式。</span><span class="sxs-lookup"><span data-stu-id="70ea9-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="70ea9-132">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="70ea9-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="70ea9-133">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="70ea9-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="70ea9-134">指定功能表項目類型的一組位旗標。</span><span class="sxs-lookup"><span data-stu-id="70ea9-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="70ea9-135">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="70ea9-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="70ea9-136">值</span><span class="sxs-lookup"><span data-stu-id="70ea9-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="70ea9-137">意義</span><span class="sxs-lookup"><span data-stu-id="70ea9-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="70ea9-138"><dt>**MFR \_END**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="70ea9-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="70ea9-139">功能表項目是此子功能表或功能表資源中的最後一個;系統會在內部使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="70ea9-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="70ea9-140"><dt>**MFR \_POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="70ea9-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="70ea9-141">功能表項目會開啟功能表或子功能表;系統會在內部使用旗標。</span><span class="sxs-lookup"><span data-stu-id="70ea9-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="70ea9-142">**menuText**</span><span class="sxs-lookup"><span data-stu-id="70ea9-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="70ea9-143">類型： **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="70ea9-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="70ea9-144">以 null 終止的 Unicode 字串，其中包含這個功能表項目的文字。</span><span class="sxs-lookup"><span data-stu-id="70ea9-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="70ea9-145">這個字串的大小沒有固定限制。</span><span class="sxs-lookup"><span data-stu-id="70ea9-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70ea9-146">備註</span><span class="sxs-lookup"><span data-stu-id="70ea9-146">Remarks</span></span>

<span data-ttu-id="70ea9-147">開啟功能表或子功能表的每個功能表項目都有一個 **POPUPMENUITEM** 結構。</span><span class="sxs-lookup"><span data-stu-id="70ea9-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="70ea9-148">藉由將 **類型** 成員設定為 **MF \_ 快顯視窗**，以及將 **resInfo** 成員中的 **MFR 快 \_** 顯位設定為0x0001，來識別這種類型的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="70ea9-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="70ea9-149">在此情況下，針對功能表或子功能表，寫入 [**RT \_ 功能表**](/windows/desktop/menurc/resource-types) 資源的最後資料是 [**MENUHELPID**](menuhelpid.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="70ea9-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="70ea9-150">**MENUHELPID** 包含可在 [**WM \_**](../shell/wm-help.md) 說明處理期間識別功能表的數值運算式。</span><span class="sxs-lookup"><span data-stu-id="70ea9-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="70ea9-151">此外，在 **resInfo** 成員中設定 **MFR 快 \_** 顯位的每個 **POPUPMENUITEM** 結構，後面都會接著 [**MENUHELPID**](menuhelpid.md)結構，再加上一個額外的 **POPUPMENUITEM** 結構，其中每個功能表項目都是該子功能表中的每個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="70ea9-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="70ea9-152">子功能表中的最後一個 **POPUPMENUITEM** 結構會在 **resInfo** 成員中設定 **MFR \_ 結束** 位。</span><span class="sxs-lookup"><span data-stu-id="70ea9-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="70ea9-153">若要找出資源的結尾，請尋找每個 **MFR \_ 快顯視窗** 的相符 **MFR \_ 端**，再加上一個符合最外層功能表項目的額外 **MFR \_ 端**。</span><span class="sxs-lookup"><span data-stu-id="70ea9-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="70ea9-154">將 **類型** 成員設定為 **MF \_ END** 以表示最後一個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="70ea9-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="70ea9-155">由於您可以嵌套子功能表，因此可能會有多個層級的 **MF \_ END**。</span><span class="sxs-lookup"><span data-stu-id="70ea9-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="70ea9-156">在這些情況下，功能表項目是連續的。</span><span class="sxs-lookup"><span data-stu-id="70ea9-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ea9-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="70ea9-157">Requirements</span></span>



| <span data-ttu-id="70ea9-158">需求</span><span class="sxs-lookup"><span data-stu-id="70ea9-158">Requirement</span></span> | <span data-ttu-id="70ea9-159">值</span><span class="sxs-lookup"><span data-stu-id="70ea9-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="70ea9-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70ea9-160">Minimum supported client</span></span><br/> | <span data-ttu-id="70ea9-161">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70ea9-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="70ea9-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70ea9-162">Minimum supported server</span></span><br/> | <span data-ttu-id="70ea9-163">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70ea9-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="70ea9-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70ea9-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="70ea9-165">**參考**</span><span class="sxs-lookup"><span data-stu-id="70ea9-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="70ea9-166">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="70ea9-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="70ea9-167">**MENUHELPID**</span><span class="sxs-lookup"><span data-stu-id="70ea9-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="70ea9-168">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="70ea9-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="70ea9-169">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="70ea9-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="70ea9-170">**概念**</span><span class="sxs-lookup"><span data-stu-id="70ea9-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="70ea9-171">資源</span><span class="sxs-lookup"><span data-stu-id="70ea9-171">Resources</span></span>](resources.md)
</dt> </dl>

 

