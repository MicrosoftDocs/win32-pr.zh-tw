---
title: 'TBN_DRAGOUT (Commctrl 的通知碼) '
description: 當使用者按一下按鈕，然後將游標移出按鈕時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024843"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="ea8dd-105">TBN \_ DRAGOUT 通知碼</span><span class="sxs-lookup"><span data-stu-id="ea8dd-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="ea8dd-106">當使用者按一下按鈕，然後將游標移出按鈕時，由工具列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="ea8dd-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ea8dd-108">參數</span><span class="sxs-lookup"><span data-stu-id="ea8dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea8dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8dd-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="ea8dd-111">針對此通知碼，只有此結構的 **hdr** 和 **iItem** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="ea8dd-112">此結構的 **iItem** 成員包含所拖曳按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8dd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea8dd-113">Return value</span></span>

<span data-ttu-id="ea8dd-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8dd-115">備註</span><span class="sxs-lookup"><span data-stu-id="ea8dd-115">Remarks</span></span>

<span data-ttu-id="ea8dd-116">此通知碼可讓應用程式執行工具列按鈕的拖放功能。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="ea8dd-117">處理此通知程式碼時，應用程式會開始拖放作業。</span><span class="sxs-lookup"><span data-stu-id="ea8dd-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8dd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea8dd-118">Requirements</span></span>



| <span data-ttu-id="ea8dd-119">需求</span><span class="sxs-lookup"><span data-stu-id="ea8dd-119">Requirement</span></span> | <span data-ttu-id="ea8dd-120">值</span><span class="sxs-lookup"><span data-stu-id="ea8dd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8dd-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea8dd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8dd-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea8dd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea8dd-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea8dd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8dd-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea8dd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea8dd-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ea8dd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea8dd-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8dd-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





