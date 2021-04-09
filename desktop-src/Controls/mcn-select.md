---
title: 'MCN_SELECT (Commctrl 的通知碼) '
description: 當使用者在月曆控制項中做出明確的日期選取時，由月曆控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024727"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="ef316-105">MCN \_ 選取通知碼</span><span class="sxs-lookup"><span data-stu-id="ef316-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="ef316-106">當使用者在月曆控制項中做出明確的日期選取時，由月曆控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="ef316-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="ef316-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ef316-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ef316-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef316-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef316-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef316-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef316-110">[**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange)結構的指標，其中包含目前所選取日期範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef316-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef316-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef316-111">Return value</span></span>

<span data-ttu-id="ef316-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ef316-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef316-113">備註</span><span class="sxs-lookup"><span data-stu-id="ef316-113">Remarks</span></span>

<span data-ttu-id="ef316-114">**MCN \_ select** 通知碼類似于 [**MCN \_ SELCHANGE**](mcn-selchange.md)，但 **MCN \_ select** 只會傳送以回應使用者的明確日期選擇。</span><span class="sxs-lookup"><span data-stu-id="ef316-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="ef316-115">**MCN \_SELCHANGE** 適用于任何選取專案變更。</span><span class="sxs-lookup"><span data-stu-id="ef316-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef316-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef316-116">Requirements</span></span>



| <span data-ttu-id="ef316-117">需求</span><span class="sxs-lookup"><span data-stu-id="ef316-117">Requirement</span></span> | <span data-ttu-id="ef316-118">值</span><span class="sxs-lookup"><span data-stu-id="ef316-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef316-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef316-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef316-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef316-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef316-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef316-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef316-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef316-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef316-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ef316-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef316-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef316-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





