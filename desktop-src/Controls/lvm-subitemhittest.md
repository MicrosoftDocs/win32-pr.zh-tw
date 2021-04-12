---
title: 'LVM_SUBITEMHITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個清單視圖專案或子專案位於指定的位置。 您可以明確地傳送此訊息，或使用 ListView \_ SubItemHitTest 宏來傳送。
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464408"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="cafed-105">LVM \_ SUBITEMHITTEST 訊息</span><span class="sxs-lookup"><span data-stu-id="cafed-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="cafed-106">判斷哪一個清單視圖專案或子專案位於指定的位置。</span><span class="sxs-lookup"><span data-stu-id="cafed-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="cafed-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="cafed-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cafed-108">參數</span><span class="sxs-lookup"><span data-stu-id="cafed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cafed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cafed-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cafed-110">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="cafed-110">Must be 0.</span></span> <span data-ttu-id="cafed-111">**Windows Vista。**</span><span class="sxs-lookup"><span data-stu-id="cafed-111">**Windows Vista.**</span></span> <span data-ttu-id="cafed-112">如果要取出 *lParam* 的 **iGroup** 成員，則應為-1。</span><span class="sxs-lookup"><span data-stu-id="cafed-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="cafed-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cafed-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cafed-114">[**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cafed-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="cafed-115">**LVHITTESTINFO** 內的 [**點**](/previous-versions//dd162805(v=vs.85))結構應設定為要進行點擊測試的用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="cafed-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cafed-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="cafed-116">Return value</span></span>

<span data-ttu-id="cafed-117">傳回已測試之專案或子專案的索引（如果有的話），否則為-1。</span><span class="sxs-lookup"><span data-stu-id="cafed-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="cafed-118">如果專案或子專案位於指定的座標， [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) 結構的欄位將會填入適用的點擊資訊。</span><span class="sxs-lookup"><span data-stu-id="cafed-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cafed-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cafed-119">Requirements</span></span>



| <span data-ttu-id="cafed-120">需求</span><span class="sxs-lookup"><span data-stu-id="cafed-120">Requirement</span></span> | <span data-ttu-id="cafed-121">值</span><span class="sxs-lookup"><span data-stu-id="cafed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cafed-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cafed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cafed-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cafed-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cafed-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cafed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cafed-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cafed-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cafed-126">標頭</span><span class="sxs-lookup"><span data-stu-id="cafed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cafed-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cafed-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

