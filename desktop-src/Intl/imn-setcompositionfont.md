---
description: 當輸入內容的字型更新時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: 'IMN_SETCOMPOSITIONFONT 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980632"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="13476-104">IMN \_ SETCOMPOSITIONFONT 通知碼</span><span class="sxs-lookup"><span data-stu-id="13476-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="13476-105">當輸入內容的字型更新時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="13476-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="13476-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="13476-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="13476-107">參數</span><span class="sxs-lookup"><span data-stu-id="13476-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13476-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="13476-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="13476-109">設定為 IMN \_ SETCOMPOSITIONFONT。</span><span class="sxs-lookup"><span data-stu-id="13476-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="13476-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="13476-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="13476-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="13476-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13476-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="13476-112">Return Value</span></span>

<span data-ttu-id="13476-113">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="13476-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13476-114">備註</span><span class="sxs-lookup"><span data-stu-id="13476-114">Remarks</span></span>

<span data-ttu-id="13476-115">應用程式可以使用 [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) 函數來取得字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13476-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="13476-116">然後，IME 視窗會使用字型來繪製組合字元串。</span><span class="sxs-lookup"><span data-stu-id="13476-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="13476-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="13476-117">Requirements</span></span>



| <span data-ttu-id="13476-118">需求</span><span class="sxs-lookup"><span data-stu-id="13476-118">Requirement</span></span> | <span data-ttu-id="13476-119">值</span><span class="sxs-lookup"><span data-stu-id="13476-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13476-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13476-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13476-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13476-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="13476-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13476-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13476-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13476-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13476-124">標頭</span><span class="sxs-lookup"><span data-stu-id="13476-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="13476-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="13476-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13476-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13476-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13476-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="13476-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="13476-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="13476-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="13476-129">**ImmGetCompositionFont**</span><span class="sxs-lookup"><span data-stu-id="13476-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="13476-130">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="13476-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




