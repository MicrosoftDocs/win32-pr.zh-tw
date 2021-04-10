---
title: 'LVM_HITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個清單視圖專案（如果有的話）位於指定的位置。 您可以明確地傳送此訊息，或使用 ListView \_ system.windows.media.visualtreehelper.hittest 宏來傳送。
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934891"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="6471c-105">LVM \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="6471c-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="6471c-106">判斷哪一個清單視圖專案（如果有的話）位於指定的位置。</span><span class="sxs-lookup"><span data-stu-id="6471c-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="6471c-107">您可以明確地傳送此訊息，或使用 [**ListView \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6471c-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6471c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6471c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6471c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6471c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6471c-110">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="6471c-110">Must be 0.</span></span> <span data-ttu-id="6471c-111">**Windows Vista。**</span><span class="sxs-lookup"><span data-stu-id="6471c-111">**Windows Vista.**</span></span> <span data-ttu-id="6471c-112">如果要取出 *lParam* 結構的 **iGroup** 和 **iSubItem** 成員，則應該是-1。</span><span class="sxs-lookup"><span data-stu-id="6471c-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="6471c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6471c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6471c-114">[**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)結構的指標，其中包含要點擊測試的位置，並接收點擊測試結果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6471c-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6471c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6471c-115">Return value</span></span>

<span data-ttu-id="6471c-116">傳回位於指定位置之專案的索引（如果有的話），否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="6471c-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6471c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6471c-117">Requirements</span></span>



| <span data-ttu-id="6471c-118">需求</span><span class="sxs-lookup"><span data-stu-id="6471c-118">Requirement</span></span> | <span data-ttu-id="6471c-119">值</span><span class="sxs-lookup"><span data-stu-id="6471c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6471c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6471c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6471c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6471c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6471c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6471c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6471c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6471c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6471c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6471c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6471c-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6471c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





