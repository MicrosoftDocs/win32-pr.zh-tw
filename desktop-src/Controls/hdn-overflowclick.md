---
title: 'HDN_OVERFLOWCLICK (Commctrl 的通知碼) '
description: 按一下標頭的溢位按鈕時，由標題控制項傳送到其父系。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843671"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="ca006-105">HDN \_ OVERFLOWCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="ca006-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="ca006-106">按一下標頭的溢位按鈕時，由標題控制項傳送到其父系。</span><span class="sxs-lookup"><span data-stu-id="ca006-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="ca006-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ca006-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ca006-108">參數</span><span class="sxs-lookup"><span data-stu-id="ca006-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca006-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ca006-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca006-110">描述通知碼的 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="ca006-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="ca006-111">呼叫進程負責配置此結構，包括包含的 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構。</span><span class="sxs-lookup"><span data-stu-id="ca006-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="ca006-112">設定 **NMHDR** 結構的成員，包括必須設定為 HDN OVERFLOWCLICK 的程式 *代碼* 成員 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ca006-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="ca006-113">將 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的 **iItem** 成員設定為不可見的第一個標題專案的索引，因此應顯示在溢位上。</span><span class="sxs-lookup"><span data-stu-id="ca006-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca006-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca006-114">Return value</span></span>

<span data-ttu-id="ca006-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ca006-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca006-116">備註</span><span class="sxs-lookup"><span data-stu-id="ca006-116">Remarks</span></span>

<span data-ttu-id="ca006-117">通知接收者會轉換 **LPARAM** 來取出 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) 結構。</span><span class="sxs-lookup"><span data-stu-id="ca006-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="ca006-118">**WPARAM** 包含傳送通知之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca006-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="ca006-119">只有當標題控制項上設定了 [**HDS \_ 溢**](header-control-styles.md) 位時，才會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ca006-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca006-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca006-120">Requirements</span></span>



| <span data-ttu-id="ca006-121">需求</span><span class="sxs-lookup"><span data-stu-id="ca006-121">Requirement</span></span> | <span data-ttu-id="ca006-122">值</span><span class="sxs-lookup"><span data-stu-id="ca006-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca006-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca006-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ca006-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca006-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca006-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca006-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ca006-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca006-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca006-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ca006-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca006-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca006-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





