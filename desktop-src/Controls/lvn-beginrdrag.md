---
title: 'LVN_BEGINRDRAG (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示正在起始涉及滑鼠右鍵的拖放作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933957"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="9bcbc-105">LVN \_ BEGINRDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="9bcbc-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="9bcbc-106">通知清單視圖控制項的父視窗，表示正在起始涉及滑鼠右鍵的拖放作業。</span><span class="sxs-lookup"><span data-stu-id="9bcbc-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="9bcbc-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="9bcbc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9bcbc-108">參數</span><span class="sxs-lookup"><span data-stu-id="9bcbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcbc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bcbc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcbc-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9bcbc-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="9bcbc-111">**IItem** 成員會識別要拖曳的專案，而其他成員則為零。</span><span class="sxs-lookup"><span data-stu-id="9bcbc-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcbc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bcbc-112">Return value</span></span>

<span data-ttu-id="9bcbc-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="9bcbc-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcbc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bcbc-114">Requirements</span></span>



| <span data-ttu-id="9bcbc-115">需求</span><span class="sxs-lookup"><span data-stu-id="9bcbc-115">Requirement</span></span> | <span data-ttu-id="9bcbc-116">值</span><span class="sxs-lookup"><span data-stu-id="9bcbc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcbc-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bcbc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcbc-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bcbc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bcbc-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bcbc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcbc-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bcbc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9bcbc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9bcbc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bcbc-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bcbc-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





