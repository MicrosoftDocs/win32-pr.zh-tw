---
title: NORMALMENUITEM 結構
description: 包含未開啟功能表或子功能表的功能表資源中，每個專案的相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- NORMALMENUITEM 結構功能表和其他資源
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317183"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="c2578-105">NORMALMENUITEM 結構</span><span class="sxs-lookup"><span data-stu-id="c2578-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="c2578-106">包含未開啟功能表或子功能表的功能表資源中，每個專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c2578-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="c2578-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="c2578-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2578-108">語法</span><span class="sxs-lookup"><span data-stu-id="c2578-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="c2578-109">成員</span><span class="sxs-lookup"><span data-stu-id="c2578-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2578-110">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="c2578-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c2578-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="c2578-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c2578-112">功能表項目的類型。</span><span class="sxs-lookup"><span data-stu-id="c2578-112">The type of menu item.</span></span> <span data-ttu-id="c2578-113">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c2578-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="c2578-114">值</span><span class="sxs-lookup"><span data-stu-id="c2578-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="c2578-115">意義</span><span class="sxs-lookup"><span data-stu-id="c2578-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="c2578-116"><dt>**MFR \_END**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="c2578-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="c2578-117">功能表項目是此子功能表或功能表資源中的最後一個;系統會在內部使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="c2578-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="c2578-118"><dt>**MFR \_POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="c2578-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="c2578-119">功能表項目會開啟功能表或子功能表;系統會在內部使用旗標。</span><span class="sxs-lookup"><span data-stu-id="c2578-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="c2578-120">**menuText**</span><span class="sxs-lookup"><span data-stu-id="c2578-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="c2578-121">類型： **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="c2578-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="c2578-122">以 null 終止的 Unicode 字串，其中包含這個功能表項目的文字。</span><span class="sxs-lookup"><span data-stu-id="c2578-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="c2578-123">這個字串的大小沒有固定限制。</span><span class="sxs-lookup"><span data-stu-id="c2578-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2578-124">備註</span><span class="sxs-lookup"><span data-stu-id="c2578-124">Remarks</span></span>

<span data-ttu-id="c2578-125">未開啟功能表或子功能表的每個功能表項目都有一個 **NORMALMENUITEM** 結構。</span><span class="sxs-lookup"><span data-stu-id="c2578-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="c2578-126">將 **resInfo** 成員設定為 **MFR \_ END**，以指出功能表上的最後一個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="c2578-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="c2578-127">功能表分隔符號是特殊類型的功能表項目，非作用中，但會顯示為兩個現用功能表項目之間的分隔線。</span><span class="sxs-lookup"><span data-stu-id="c2578-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="c2578-128">藉由將 **menuText** 成員保留空白來表示功能表分隔符號。</span><span class="sxs-lookup"><span data-stu-id="c2578-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2578-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2578-129">Requirements</span></span>



| <span data-ttu-id="c2578-130">需求</span><span class="sxs-lookup"><span data-stu-id="c2578-130">Requirement</span></span> | <span data-ttu-id="c2578-131">值</span><span class="sxs-lookup"><span data-stu-id="c2578-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2578-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2578-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c2578-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2578-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2578-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2578-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c2578-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2578-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c2578-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2578-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2578-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="c2578-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2578-138">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="c2578-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="c2578-139">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="c2578-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="c2578-140">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="c2578-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="c2578-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="c2578-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c2578-142">資源</span><span class="sxs-lookup"><span data-stu-id="c2578-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





