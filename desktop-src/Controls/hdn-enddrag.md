---
title: 'HDN_ENDDRAG (Commctrl 的通知碼) '
description: 當拖曳作業在其中一個專案上結束時，由標題控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。 只有設定為 HDS System.windows.dragdrop.drop> 樣式的標題控制項才會 \_ 傳送此通知碼。
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467124"
---
# <a name="hdn_enddrag-notification-code"></a><span data-ttu-id="459ab-106">HDN \_ ENDDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="459ab-106">HDN\_ENDDRAG notification code</span></span>

<span data-ttu-id="459ab-107">當拖曳作業在其中一個專案上結束時，由標題控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="459ab-107">Sent by a header control when a drag operation has ended on one of its items.</span></span> <span data-ttu-id="459ab-108">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="459ab-108">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="459ab-109">只有設定為 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="459ab-109">Only header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="459ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="459ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="459ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="459ab-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459ab-112">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含所要拖曳之標頭專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="459ab-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that was being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="459ab-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="459ab-113">Return value</span></span>

<span data-ttu-id="459ab-114">若要允許控制項自動放置和重新排序專案，請傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="459ab-114">To allow the control to automatically place and reorder the item, return **FALSE**.</span></span> <span data-ttu-id="459ab-115">若要避免放置專案，請傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="459ab-115">To prevent the item from being placed, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="459ab-116">備註</span><span class="sxs-lookup"><span data-stu-id="459ab-116">Remarks</span></span>

<span data-ttu-id="459ab-117">如果擁有者正在執行外部 (手動) 拖放管理，它必須傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="459ab-117">If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**.</span></span> <span data-ttu-id="459ab-118">然後，擁有者必須藉由傳送 [**HDM \_ SETITEM**](hdm-setitem.md) 或 [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md)，手動重新排序標頭專案。</span><span class="sxs-lookup"><span data-stu-id="459ab-118">The owner then must reorder header items manually by sending [**HDM\_SETITEM**](hdm-setitem.md) or [**HDM\_SETORDERARRAY**](hdm-setorderarray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="459ab-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="459ab-119">Requirements</span></span>



| <span data-ttu-id="459ab-120">需求</span><span class="sxs-lookup"><span data-stu-id="459ab-120">Requirement</span></span> | <span data-ttu-id="459ab-121">值</span><span class="sxs-lookup"><span data-stu-id="459ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="459ab-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="459ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="459ab-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="459ab-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="459ab-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="459ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="459ab-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="459ab-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="459ab-126">標頭</span><span class="sxs-lookup"><span data-stu-id="459ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="459ab-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="459ab-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





