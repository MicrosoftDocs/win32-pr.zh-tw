---
title: 'TVM_GETISEARCHSTRING 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項的累加式搜尋字串。
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105959"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="fa537-104">TVM \_ GETISEARCHSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="fa537-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="fa537-105">抓取樹狀檢視控制項的累加式搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="fa537-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="fa537-106">樹狀檢視控制項會使用增量搜尋字串，根據使用者輸入的字元來選取專案。</span><span class="sxs-lookup"><span data-stu-id="fa537-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="fa537-107">您可以使用 [**TreeView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fa537-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa537-108">參數</span><span class="sxs-lookup"><span data-stu-id="fa537-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa537-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa537-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa537-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fa537-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fa537-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa537-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa537-112">接收累加式搜尋字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="fa537-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa537-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa537-113">Return value</span></span>

<span data-ttu-id="fa537-114">傳回增量搜尋字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="fa537-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa537-115">備註</span><span class="sxs-lookup"><span data-stu-id="fa537-115">Remarks</span></span>

<span data-ttu-id="fa537-116">**安全性警告：** 不當使用此訊息可能會危及程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="fa537-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="fa537-117">您必須配置夠大的緩衝區來保存字串。</span><span class="sxs-lookup"><span data-stu-id="fa537-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="fa537-118">首先，在 *lParam* 中呼叫傳遞 **Null** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="fa537-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="fa537-119">這會傳回所需的字元數，但不包括 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fa537-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="fa537-120">然後第二次呼叫訊息以抓取字串。</span><span class="sxs-lookup"><span data-stu-id="fa537-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="fa537-121">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="fa537-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="fa537-122">如果樹狀檢視控制項不在累加式搜尋模式中，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="fa537-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa537-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa537-123">Requirements</span></span>



| <span data-ttu-id="fa537-124">需求</span><span class="sxs-lookup"><span data-stu-id="fa537-124">Requirement</span></span> | <span data-ttu-id="fa537-125">值</span><span class="sxs-lookup"><span data-stu-id="fa537-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa537-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa537-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa537-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa537-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa537-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa537-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa537-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa537-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa537-130">標頭</span><span class="sxs-lookup"><span data-stu-id="fa537-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa537-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa537-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fa537-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="fa537-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa537-133">**TVM \_GETISEARCHSTRINGW** (Unicode) 和 **TVM \_ GETISEARCHSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="fa537-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





