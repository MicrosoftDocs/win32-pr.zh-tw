---
description: 當候選處理完成，而且 IME 即將移動候選視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: 'IMN_SETCANDIDATEPOS 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971824"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="7f3fd-104">IMN \_ SETCANDIDATEPOS 通知碼</span><span class="sxs-lookup"><span data-stu-id="7f3fd-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="7f3fd-105">當候選處理完成，而且 IME 即將移動候選視窗時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="7f3fd-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="7f3fd-107">參數</span><span class="sxs-lookup"><span data-stu-id="7f3fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3fd-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f3fd-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7f3fd-109">設定為 IMN \_ SETCANDIDATEPOS。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="7f3fd-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f3fd-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7f3fd-111">候選清單旗標。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-111">Candidate list flag.</span></span> <span data-ttu-id="7f3fd-112">每個位都對應至候選清單： bit 0 到第一個清單，第1個到第二個，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="7f3fd-113">如果指定的位為1，則對應的候選視窗即將移動。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3fd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f3fd-114">Return Value</span></span>

<span data-ttu-id="7f3fd-115">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f3fd-116">備註</span><span class="sxs-lookup"><span data-stu-id="7f3fd-116">Remarks</span></span>

<span data-ttu-id="7f3fd-117">應用程式應該在顯示候選視窗本身時處理此命令。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="7f3fd-118">在處理此命令時，IME 視窗會移動候選視窗。</span><span class="sxs-lookup"><span data-stu-id="7f3fd-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3fd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f3fd-119">Requirements</span></span>



| <span data-ttu-id="7f3fd-120">需求</span><span class="sxs-lookup"><span data-stu-id="7f3fd-120">Requirement</span></span> | <span data-ttu-id="7f3fd-121">值</span><span class="sxs-lookup"><span data-stu-id="7f3fd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3fd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f3fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3fd-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f3fd-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7f3fd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f3fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3fd-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f3fd-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f3fd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="7f3fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f3fd-127"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f3fd-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3fd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f3fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3fd-129">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="7f3fd-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7f3fd-130">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="7f3fd-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="7f3fd-131">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="7f3fd-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




