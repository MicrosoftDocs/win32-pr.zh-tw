---
title: 'LVM_SETHOVERTIME 訊息 (Commctrl .h) '
description: 設定在選取專案之前，滑鼠游標必須停留在專案上的時間量。 您可以明確地傳送此訊息，或使用 ListView \_ SetHoverTime 宏。
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093835"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="f9057-105">LVM \_ SETHOVERTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="f9057-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="f9057-106">設定在選取專案之前，滑鼠游標必須停留在專案上的時間量。</span><span class="sxs-lookup"><span data-stu-id="f9057-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="f9057-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) 宏。</span><span class="sxs-lookup"><span data-stu-id="f9057-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9057-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9057-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9057-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9057-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f9057-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f9057-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f9057-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9057-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9057-112">在選取專案之前，滑鼠游標必須停留在某個專案上的新時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f9057-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="f9057-113">如果這個值是 (**DWORD**) -1，則會將暫留時間設定為預設的停留時間。</span><span class="sxs-lookup"><span data-stu-id="f9057-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9057-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9057-114">Return value</span></span>

<span data-ttu-id="f9057-115">傳回先前的停留時間。</span><span class="sxs-lookup"><span data-stu-id="f9057-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9057-116">備註</span><span class="sxs-lookup"><span data-stu-id="f9057-116">Remarks</span></span>

<span data-ttu-id="f9057-117">暫止的時間只會影響具有 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md)、 [**lvs) \_ ex \_ ONECLICKACTI加值稅E**](extended-list-view-styles.md)或 [**lvs) \_ ex \_ TWOCLICKACTI加值稅E**](extended-list-view-styles.md) 擴充清單視圖樣式的清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="f9057-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9057-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9057-118">Requirements</span></span>



| <span data-ttu-id="f9057-119">需求</span><span class="sxs-lookup"><span data-stu-id="f9057-119">Requirement</span></span> | <span data-ttu-id="f9057-120">值</span><span class="sxs-lookup"><span data-stu-id="f9057-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9057-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9057-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9057-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9057-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9057-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9057-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9057-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9057-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9057-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f9057-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9057-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9057-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





