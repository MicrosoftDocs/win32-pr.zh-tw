---
title: 'PSN_HELP (Prsht.idl 的通知碼) '
description: 通知頁面，表示使用者已按一下 [說明] 按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967344"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="53378-105">PSN 說明 \_ 通知碼</span><span class="sxs-lookup"><span data-stu-id="53378-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="53378-106">通知頁面，表示使用者已按一下 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="53378-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="53378-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="53378-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="53378-108">參數</span><span class="sxs-lookup"><span data-stu-id="53378-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53378-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53378-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53378-110">[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="53378-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="53378-111">此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53378-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="53378-112">**PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。</span><span class="sxs-lookup"><span data-stu-id="53378-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53378-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="53378-113">Return value</span></span>

<span data-ttu-id="53378-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="53378-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53378-115">備註</span><span class="sxs-lookup"><span data-stu-id="53378-115">Remarks</span></span>

<span data-ttu-id="53378-116">應用程式應該會顯示頁面的說明資訊。</span><span class="sxs-lookup"><span data-stu-id="53378-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="53378-117">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。</span><span class="sxs-lookup"><span data-stu-id="53378-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53378-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="53378-118">Requirements</span></span>



| <span data-ttu-id="53378-119">需求</span><span class="sxs-lookup"><span data-stu-id="53378-119">Requirement</span></span> | <span data-ttu-id="53378-120">值</span><span class="sxs-lookup"><span data-stu-id="53378-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53378-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53378-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53378-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53378-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="53378-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53378-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53378-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53378-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="53378-125">標頭</span><span class="sxs-lookup"><span data-stu-id="53378-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="53378-126"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="53378-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





