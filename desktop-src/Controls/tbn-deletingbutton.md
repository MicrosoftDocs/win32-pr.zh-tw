---
title: 'TBN_DELETINGBUTTON 訊息 (Commctrl .h) '
description: 工具列控制項在即將刪除按鈕時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- TBN_DELETINGBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508396"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="a0ee6-105">TBN \_ DELETINGBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="a0ee6-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="a0ee6-106">工具列控制項在即將刪除按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="a0ee6-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="a0ee6-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a0ee6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a0ee6-108">參數</span><span class="sxs-lookup"><span data-stu-id="a0ee6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ee6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0ee6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0ee6-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標，其中包含要刪除之按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0ee6-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="a0ee6-111">針對此通知碼，只有此結構的 **hdr** 和 **iItem** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="a0ee6-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="a0ee6-112">此結構的 **iItem** 成員包含所要刪除按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0ee6-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ee6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0ee6-113">Return value</span></span>

<span data-ttu-id="a0ee6-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a0ee6-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ee6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0ee6-115">Requirements</span></span>



| <span data-ttu-id="a0ee6-116">需求</span><span class="sxs-lookup"><span data-stu-id="a0ee6-116">Requirement</span></span> | <span data-ttu-id="a0ee6-117">值</span><span class="sxs-lookup"><span data-stu-id="a0ee6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ee6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0ee6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ee6-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0ee6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0ee6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0ee6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ee6-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0ee6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0ee6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a0ee6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0ee6-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0ee6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





