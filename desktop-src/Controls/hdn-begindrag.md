---
title: 'HDN_BEGINDRAG (Commctrl 的通知碼) '
description: 當拖曳作業在其中一個專案上開始時，由標題控制項所傳送。 只有設定為 HDS System.windows.dragdrop.drop> 樣式的標題控制項才會傳送此通知碼 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025028"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="856b1-106">HDN \_ BEGINDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="856b1-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="856b1-107">當拖曳作業在其中一個專案上開始時，由標題控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="856b1-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="856b1-108">只有設定為 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="856b1-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="856b1-109">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="856b1-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="856b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="856b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856b1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="856b1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="856b1-112">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含正在拖曳之標頭專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="856b1-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="856b1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="856b1-113">Return value</span></span>

<span data-ttu-id="856b1-114">若要允許標題控制項自動管理拖放作業，請傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="856b1-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="856b1-115">如果控制項的擁有者以手動方式執行拖放重新排列，則傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="856b1-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="856b1-116">備註</span><span class="sxs-lookup"><span data-stu-id="856b1-116">Remarks</span></span>

<span data-ttu-id="856b1-117">標題控制項預設會自動管理拖放重新排列。</span><span class="sxs-lookup"><span data-stu-id="856b1-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="856b1-118">傳回 **TRUE** 表示外部 (手動) 拖放管理可讓控制項的擁有者在拖放程式中提供自訂的服務。</span><span class="sxs-lookup"><span data-stu-id="856b1-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="856b1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="856b1-119">Requirements</span></span>



| <span data-ttu-id="856b1-120">需求</span><span class="sxs-lookup"><span data-stu-id="856b1-120">Requirement</span></span> | <span data-ttu-id="856b1-121">值</span><span class="sxs-lookup"><span data-stu-id="856b1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="856b1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="856b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="856b1-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="856b1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="856b1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="856b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="856b1-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="856b1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="856b1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="856b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="856b1-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="856b1-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





