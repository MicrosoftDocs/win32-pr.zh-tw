---
title: 'LVN_COLUMNCLICK (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗：當清單視圖控制項處於報表模式時，已按下資料行標頭。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024658"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="dac7b-105">LVN \_ COLUMNCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="dac7b-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="dac7b-106">通知清單視圖控制項的父視窗：當清單視圖控制項處於報表模式時，已按下資料行標頭。</span><span class="sxs-lookup"><span data-stu-id="dac7b-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="dac7b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="dac7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dac7b-108">參數</span><span class="sxs-lookup"><span data-stu-id="dac7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dac7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dac7b-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dac7b-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="dac7b-111">**IItem** 成員為-1，而 **iSubItem** 成員會識別資料行。</span><span class="sxs-lookup"><span data-stu-id="dac7b-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="dac7b-112">所有其他成員都是零。</span><span class="sxs-lookup"><span data-stu-id="dac7b-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac7b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dac7b-113">Return value</span></span>

<span data-ttu-id="dac7b-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="dac7b-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac7b-115">備註</span><span class="sxs-lookup"><span data-stu-id="dac7b-115">Remarks</span></span>

<span data-ttu-id="dac7b-116">使用標題控制項格式（例如 [HDF \_ ] 核取方塊）來修改清單視圖控制項中的資料行標頭格式，會導致控制項在按一下標頭專案時，傳送 [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) 通知碼，而不是 LVN \_ COLUMNCLICK。</span><span class="sxs-lookup"><span data-stu-id="dac7b-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac7b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dac7b-117">Requirements</span></span>



| <span data-ttu-id="dac7b-118">需求</span><span class="sxs-lookup"><span data-stu-id="dac7b-118">Requirement</span></span> | <span data-ttu-id="dac7b-119">值</span><span class="sxs-lookup"><span data-stu-id="dac7b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dac7b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dac7b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dac7b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dac7b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dac7b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dac7b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dac7b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dac7b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dac7b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dac7b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac7b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dac7b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





