---
description: 當 IME 即將開啟候選視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: 'IMN_OPENCANDIDATE 事件 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849478"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="e99ee-104">IMN \_ OPENCANDIDATE 事件</span><span class="sxs-lookup"><span data-stu-id="e99ee-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="e99ee-105">當 IME 即將開啟候選視窗時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="e99ee-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="e99ee-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="e99ee-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="e99ee-107">參數</span><span class="sxs-lookup"><span data-stu-id="e99ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99ee-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e99ee-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e99ee-109">設定為 IMN \_ OPENCANDIDATE。</span><span class="sxs-lookup"><span data-stu-id="e99ee-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="e99ee-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e99ee-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e99ee-111">候選清單旗標。</span><span class="sxs-lookup"><span data-stu-id="e99ee-111">Candidate list flag.</span></span> <span data-ttu-id="e99ee-112">每個位都對應至候選清單： bit 0 到第一個清單，第1個到第二個，依此類推。</span><span class="sxs-lookup"><span data-stu-id="e99ee-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="e99ee-113">如果指定的位為1，則會開啟對應的候選視窗。</span><span class="sxs-lookup"><span data-stu-id="e99ee-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99ee-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e99ee-114">Return Value</span></span>

<span data-ttu-id="e99ee-115">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e99ee-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e99ee-116">備註</span><span class="sxs-lookup"><span data-stu-id="e99ee-116">Remarks</span></span>

<span data-ttu-id="e99ee-117">如果應用程式顯示候選項本身，就應該處理這個命令。</span><span class="sxs-lookup"><span data-stu-id="e99ee-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="e99ee-118">應用程式可以使用 [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) 函式來取得要顯示的候選清單。</span><span class="sxs-lookup"><span data-stu-id="e99ee-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="e99ee-119">根據預設，IME 視窗在處理此命令時，會建立候選視窗。</span><span class="sxs-lookup"><span data-stu-id="e99ee-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="e99ee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e99ee-120">Requirements</span></span>



| <span data-ttu-id="e99ee-121">需求</span><span class="sxs-lookup"><span data-stu-id="e99ee-121">Requirement</span></span> | <span data-ttu-id="e99ee-122">值</span><span class="sxs-lookup"><span data-stu-id="e99ee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e99ee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e99ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e99ee-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e99ee-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e99ee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e99ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e99ee-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e99ee-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e99ee-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e99ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e99ee-128"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e99ee-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e99ee-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e99ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99ee-130">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="e99ee-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e99ee-131">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="e99ee-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e99ee-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="e99ee-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="e99ee-133">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="e99ee-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




