---
description: 當 IME 即將顯示錯誤訊息或其他資訊時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: 'IMN_GUIDELINE 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319283"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="1d370-104">IMN \_ 指導方針碼</span><span class="sxs-lookup"><span data-stu-id="1d370-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="1d370-105">當 IME 即將顯示錯誤訊息或其他資訊時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="1d370-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="1d370-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1d370-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="1d370-107">參數</span><span class="sxs-lookup"><span data-stu-id="1d370-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d370-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d370-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1d370-109">設定為 IMN \_ 指導方針。</span><span class="sxs-lookup"><span data-stu-id="1d370-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="1d370-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d370-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1d370-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="1d370-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d370-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d370-112">Return Value</span></span>

<span data-ttu-id="1d370-113">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1d370-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d370-114">備註</span><span class="sxs-lookup"><span data-stu-id="1d370-114">Remarks</span></span>

<span data-ttu-id="1d370-115">應用程式會藉由呼叫 [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) 函式來取得錯誤訊息或 IME 中的資訊來處理此命令。</span><span class="sxs-lookup"><span data-stu-id="1d370-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="1d370-116">IME 視窗會在資訊視窗中顯示錯誤訊息或資訊字串。</span><span class="sxs-lookup"><span data-stu-id="1d370-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d370-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d370-117">Requirements</span></span>



| <span data-ttu-id="1d370-118">需求</span><span class="sxs-lookup"><span data-stu-id="1d370-118">Requirement</span></span> | <span data-ttu-id="1d370-119">值</span><span class="sxs-lookup"><span data-stu-id="1d370-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d370-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d370-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d370-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d370-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1d370-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d370-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d370-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d370-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d370-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1d370-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d370-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1d370-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d370-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d370-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d370-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="1d370-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1d370-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="1d370-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1d370-129">**ImmGetGuideLine**</span><span class="sxs-lookup"><span data-stu-id="1d370-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="1d370-130">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="1d370-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




