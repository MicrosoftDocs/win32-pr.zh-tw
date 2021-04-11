---
description: 當 IME 即將變更候選視窗的內容時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: 'IMN_CHANGECANDIDATE 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115624"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="53c07-104">IMN \_ CHANGECANDIDATE 通知碼</span><span class="sxs-lookup"><span data-stu-id="53c07-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="53c07-105">當 IME 即將變更候選視窗的內容時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="53c07-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="53c07-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="53c07-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="53c07-107">參數</span><span class="sxs-lookup"><span data-stu-id="53c07-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c07-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="53c07-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="53c07-109">設定為 IMN \_ CHANGECANDIDATE。</span><span class="sxs-lookup"><span data-stu-id="53c07-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="53c07-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="53c07-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="53c07-111">候選清單旗標。</span><span class="sxs-lookup"><span data-stu-id="53c07-111">Candidate list flag.</span></span> <span data-ttu-id="53c07-112">每個位都對應至候選清單： bit 0 到第一個清單、位1到第二個清單等等。</span><span class="sxs-lookup"><span data-stu-id="53c07-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="53c07-113">如果指定的位為1，則對應的候選視窗即將變更。</span><span class="sxs-lookup"><span data-stu-id="53c07-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c07-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="53c07-114">Return Value</span></span>

<span data-ttu-id="53c07-115">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="53c07-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c07-116">備註</span><span class="sxs-lookup"><span data-stu-id="53c07-116">Remarks</span></span>

<span data-ttu-id="53c07-117">如果應用程式顯示候選項本身，就應該處理這個命令。</span><span class="sxs-lookup"><span data-stu-id="53c07-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="53c07-118">在處理此命令時，IME 視窗會變更候選視窗的外觀。</span><span class="sxs-lookup"><span data-stu-id="53c07-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="53c07-119">應用程式可以使用 [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)和 [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)來取得系統視窗的相關資訊</span><span class="sxs-lookup"><span data-stu-id="53c07-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="53c07-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="53c07-120">Requirements</span></span>



| <span data-ttu-id="53c07-121">需求</span><span class="sxs-lookup"><span data-stu-id="53c07-121">Requirement</span></span> | <span data-ttu-id="53c07-122">值</span><span class="sxs-lookup"><span data-stu-id="53c07-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c07-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53c07-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53c07-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53c07-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="53c07-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53c07-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53c07-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53c07-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53c07-127">標頭</span><span class="sxs-lookup"><span data-stu-id="53c07-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c07-128"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="53c07-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c07-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53c07-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c07-130">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="53c07-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="53c07-131">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="53c07-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="53c07-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="53c07-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="53c07-133">**ImmGetCandidateListCount**</span><span class="sxs-lookup"><span data-stu-id="53c07-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="53c07-134">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="53c07-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




