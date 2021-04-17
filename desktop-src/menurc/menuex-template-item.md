---
title: MENUEX_TEMPLATE_ITEM 結構
description: 定義擴充功能表範本中的功能表項目。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509188"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="cc77f-105">MENUEX \_ 範本 \_ 專案結構</span><span class="sxs-lookup"><span data-stu-id="cc77f-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="cc77f-106">定義擴充功能表範本中的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="cc77f-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="cc77f-107">此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="cc77f-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc77f-108">語法</span><span class="sxs-lookup"><span data-stu-id="cc77f-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="cc77f-109">成員</span><span class="sxs-lookup"><span data-stu-id="cc77f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc77f-110">**dwType**</span><span class="sxs-lookup"><span data-stu-id="cc77f-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc77f-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cc77f-112">功能表項目類型。</span><span class="sxs-lookup"><span data-stu-id="cc77f-112">The menu item type.</span></span> <span data-ttu-id="cc77f-113">這個成員可以是類型 (開頭是與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) 結構一起列出的 MFT) 值的組合。</span><span class="sxs-lookup"><span data-stu-id="cc77f-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc77f-114">**dwState**</span><span class="sxs-lookup"><span data-stu-id="cc77f-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc77f-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cc77f-116">功能表項目的狀態。</span><span class="sxs-lookup"><span data-stu-id="cc77f-116">The menu item state.</span></span> <span data-ttu-id="cc77f-117">這個成員可以是狀態 (的組合，其開頭為 MFS) 與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) 結構一起列出的值。</span><span class="sxs-lookup"><span data-stu-id="cc77f-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc77f-118">**Uid**</span><span class="sxs-lookup"><span data-stu-id="cc77f-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-119">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="cc77f-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="cc77f-120">功能表項目識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc77f-120">The menu item identifier.</span></span> <span data-ttu-id="cc77f-121">這是用來識別功能表項目的應用程式定義值。</span><span class="sxs-lookup"><span data-stu-id="cc77f-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="cc77f-122">在擴充功能表資源中，開啟下拉式功能表或子功能表，以及命令專案的專案都可以有識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc77f-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cc77f-123">**wFlags**</span><span class="sxs-lookup"><span data-stu-id="cc77f-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-124">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="cc77f-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cc77f-125">指定功能表項目是功能表列、下拉式功能表、子功能表或快捷方式功能表中的最後一個專案，以及是否為開啟下拉式功能表或子功能表的專案。</span><span class="sxs-lookup"><span data-stu-id="cc77f-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="cc77f-126">這個成員可以是零或多個這些值。</span><span class="sxs-lookup"><span data-stu-id="cc77f-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="cc77f-127">若為32位應用程式，這個成員是一個字;若是16位應用程式，則是位元組。</span><span class="sxs-lookup"><span data-stu-id="cc77f-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="cc77f-128">0x80</span><span class="sxs-lookup"><span data-stu-id="cc77f-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-129">結構會定義功能表列、下拉式功能表、子功能表或快捷方式功能表中的最後一個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="cc77f-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="cc77f-130">0x01</span><span class="sxs-lookup"><span data-stu-id="cc77f-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-131">結構會定義開啟下拉式功能表或子功能表的專案。</span><span class="sxs-lookup"><span data-stu-id="cc77f-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="cc77f-132">後續的結構會在對應的下拉式功能表或子功能表中定義功能表項目。</span><span class="sxs-lookup"><span data-stu-id="cc77f-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cc77f-133">**szText**</span><span class="sxs-lookup"><span data-stu-id="cc77f-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="cc77f-134">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="cc77f-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="cc77f-135">功能表項目文字。</span><span class="sxs-lookup"><span data-stu-id="cc77f-135">The menu item text.</span></span> <span data-ttu-id="cc77f-136">這個成員是以 null 結束的 Unicode 字串，在字邊界上對齊。</span><span class="sxs-lookup"><span data-stu-id="cc77f-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="cc77f-137">功能表項目定義的大小會根據此字串的長度而有所不同。</span><span class="sxs-lookup"><span data-stu-id="cc77f-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc77f-138">備註</span><span class="sxs-lookup"><span data-stu-id="cc77f-138">Remarks</span></span>

<span data-ttu-id="cc77f-139">擴充功能表範本包含 [**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md) 結構，後面接著一個或多個連續的 **MENUEX \_ 範本 \_ 專案** 結構。</span><span class="sxs-lookup"><span data-stu-id="cc77f-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="cc77f-140">**MENUEX \_ 範本 \_ 專案** 結構（長度為變數）會對齊 **DWORD** 界限。</span><span class="sxs-lookup"><span data-stu-id="cc77f-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="cc77f-141">若要從記憶體中的擴充功能表範本建立功能表，請使用 [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) 函數。</span><span class="sxs-lookup"><span data-stu-id="cc77f-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc77f-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc77f-142">Requirements</span></span>



| <span data-ttu-id="cc77f-143">需求</span><span class="sxs-lookup"><span data-stu-id="cc77f-143">Requirement</span></span> | <span data-ttu-id="cc77f-144">值</span><span class="sxs-lookup"><span data-stu-id="cc77f-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cc77f-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc77f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="cc77f-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc77f-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cc77f-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc77f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="cc77f-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc77f-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cc77f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc77f-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc77f-150">**參考**</span><span class="sxs-lookup"><span data-stu-id="cc77f-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc77f-151">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="cc77f-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="cc77f-152">**MENUEX \_ 範本 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="cc77f-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="cc77f-153">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="cc77f-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="cc77f-154">**概念**</span><span class="sxs-lookup"><span data-stu-id="cc77f-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cc77f-155">功能表</span><span class="sxs-lookup"><span data-stu-id="cc77f-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





