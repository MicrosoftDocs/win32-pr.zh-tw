---
description: 當 IME 即將關閉候選視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: 'IMN_CLOSECANDIDATE 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971826"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="159b8-104">IMN \_ CLOSECANDIDATE 通知碼</span><span class="sxs-lookup"><span data-stu-id="159b8-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="159b8-105">當 IME 即將關閉候選視窗時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="159b8-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="159b8-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="159b8-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="159b8-107">參數</span><span class="sxs-lookup"><span data-stu-id="159b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159b8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="159b8-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="159b8-109">設定為 IMN \_ CLOSECANDIDATE。</span><span class="sxs-lookup"><span data-stu-id="159b8-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="159b8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="159b8-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="159b8-111">候選清單旗標。</span><span class="sxs-lookup"><span data-stu-id="159b8-111">Candidate list flag.</span></span> <span data-ttu-id="159b8-112">每個位都對應至候選清單： bit 0 到第一個清單，第1個到第二個，依此類推。</span><span class="sxs-lookup"><span data-stu-id="159b8-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="159b8-113">如果指定的位為1，則對應的候選視窗即將關閉。</span><span class="sxs-lookup"><span data-stu-id="159b8-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159b8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="159b8-114">Return Value</span></span>

<span data-ttu-id="159b8-115">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="159b8-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="159b8-116">備註</span><span class="sxs-lookup"><span data-stu-id="159b8-116">Remarks</span></span>

<span data-ttu-id="159b8-117">如果應用程式顯示候選項本身，就應該處理這個命令。</span><span class="sxs-lookup"><span data-stu-id="159b8-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="159b8-118">根據預設，IME 視窗會在處理此命令時終結候選視窗。</span><span class="sxs-lookup"><span data-stu-id="159b8-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="159b8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="159b8-119">Requirements</span></span>



| <span data-ttu-id="159b8-120">需求</span><span class="sxs-lookup"><span data-stu-id="159b8-120">Requirement</span></span> | <span data-ttu-id="159b8-121">值</span><span class="sxs-lookup"><span data-stu-id="159b8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159b8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="159b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="159b8-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="159b8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="159b8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="159b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="159b8-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="159b8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="159b8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="159b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="159b8-127"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="159b8-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="159b8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="159b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159b8-129">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="159b8-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="159b8-130">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="159b8-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="159b8-131">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="159b8-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




