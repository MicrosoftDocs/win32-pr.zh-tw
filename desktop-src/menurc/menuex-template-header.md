---
title: MENUEX_TEMPLATE_HEADER 結構
description: 定義擴充功能表範本的標頭。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969960"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="98a32-105">MENUEX \_ 範本 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="98a32-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="98a32-106">定義擴充功能表範本的標頭。</span><span class="sxs-lookup"><span data-stu-id="98a32-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="98a32-107">此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="98a32-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a32-108">語法</span><span class="sxs-lookup"><span data-stu-id="98a32-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="98a32-109">成員</span><span class="sxs-lookup"><span data-stu-id="98a32-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="98a32-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="98a32-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="98a32-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="98a32-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="98a32-112">範本版本號碼。</span><span class="sxs-lookup"><span data-stu-id="98a32-112">The template version number.</span></span> <span data-ttu-id="98a32-113">擴充功能表範本的這個成員必須是1。</span><span class="sxs-lookup"><span data-stu-id="98a32-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="98a32-114">**wOffset**</span><span class="sxs-lookup"><span data-stu-id="98a32-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="98a32-115">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="98a32-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="98a32-116">相對於此結構成員結尾的第一個 [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md) 結構的位移。</span><span class="sxs-lookup"><span data-stu-id="98a32-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="98a32-117">如果第一個專案定義緊接在 **dwHelpId** 成員之後，這個成員應該是4。</span><span class="sxs-lookup"><span data-stu-id="98a32-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="98a32-118">**dwHelpId**</span><span class="sxs-lookup"><span data-stu-id="98a32-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="98a32-119">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="98a32-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="98a32-120">功能表列的說明識別碼。</span><span class="sxs-lookup"><span data-stu-id="98a32-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98a32-121">備註</span><span class="sxs-lookup"><span data-stu-id="98a32-121">Remarks</span></span>

<span data-ttu-id="98a32-122">擴充功能表範本包含 **MENUEX \_ 範本 \_ 標頭** 結構，後面接著一個或多個連續的 [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="98a32-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="98a32-123">**MENUEX \_ 範本 \_ 專案** 結構（長度為變數）會對齊 **DWORD** 界限。</span><span class="sxs-lookup"><span data-stu-id="98a32-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="98a32-124">若要從記憶體中的擴充功能表範本建立功能表，請使用 [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) 函數。</span><span class="sxs-lookup"><span data-stu-id="98a32-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a32-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="98a32-125">Requirements</span></span>



| <span data-ttu-id="98a32-126">需求</span><span class="sxs-lookup"><span data-stu-id="98a32-126">Requirement</span></span> | <span data-ttu-id="98a32-127">值</span><span class="sxs-lookup"><span data-stu-id="98a32-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="98a32-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98a32-128">Minimum supported client</span></span><br/> | <span data-ttu-id="98a32-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98a32-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98a32-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98a32-130">Minimum supported server</span></span><br/> | <span data-ttu-id="98a32-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98a32-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="98a32-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98a32-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="98a32-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="98a32-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98a32-134">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="98a32-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="98a32-135">**MENUEX \_ 範本 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="98a32-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="98a32-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="98a32-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98a32-137">功能表</span><span class="sxs-lookup"><span data-stu-id="98a32-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





