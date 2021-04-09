---
description: 當 IME 需要變更 RECONVERTSTRING 結構時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: 'IMR_CONFIRMRECONVERTSTRING 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692971"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="49cee-104">IMR \_ CONFIRMRECONVERTSTRING 通知碼</span><span class="sxs-lookup"><span data-stu-id="49cee-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="49cee-105">當 IME 需要變更 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="49cee-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="49cee-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="49cee-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="49cee-107">參數</span><span class="sxs-lookup"><span data-stu-id="49cee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49cee-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="49cee-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="49cee-109">設定為 IMR \_ CONFIRMRECONVERTSTRING。</span><span class="sxs-lookup"><span data-stu-id="49cee-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="49cee-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="49cee-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="49cee-111">輸入法中 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="49cee-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="49cee-112">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="49cee-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49cee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="49cee-113">Return Value</span></span>

<span data-ttu-id="49cee-114">如果應用程式接受已變更的 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="49cee-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="49cee-115">否則，此命令會傳回0，且 IME 會使用原始的 **RECONVERTSTRING** 結構。</span><span class="sxs-lookup"><span data-stu-id="49cee-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="49cee-116">備註</span><span class="sxs-lookup"><span data-stu-id="49cee-116">Remarks</span></span>

<span data-ttu-id="49cee-117">應用程式會在收到 [IMR \_ RECONVERTSTRING](imr-reconvertstring.md)命令時填入 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)結構。</span><span class="sxs-lookup"><span data-stu-id="49cee-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="49cee-118">在應用程式處理 [IMR \_ RECONVERTSTRING](imr-reconvertstring.md)之後，IME 可能會或可能不會調整 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構。</span><span class="sxs-lookup"><span data-stu-id="49cee-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="49cee-119">IME 傳送 WM \_ ime \_ 要求與 **IMR \_ CONFIRMRECONVERTSTRING** ，以確認 **RECONVERTSTRING** 結構的變更。</span><span class="sxs-lookup"><span data-stu-id="49cee-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="49cee-120">如果應用程式針對 **IMR \_ CONFIRMRECONVERTSTRING** 傳回 **TRUE** ，則 IME 會根據 **IMR \_ CONFIRMRECONVERTSTRING** 命令的 **RECONVERTSTRING** 結構來產生新的組合字元串。</span><span class="sxs-lookup"><span data-stu-id="49cee-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="49cee-121">如果應用程式針對 **IMR \_ CONFIRMRECONVERTSTRING** 傳回 **FALSE** ，則 IME 會根據 IMR RECONVERTSTRING 命令中的應用程式所指定的原始 **RECONVERTSTRING** 結構，產生新的組合字元串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="49cee-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cee-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="49cee-122">Requirements</span></span>



| <span data-ttu-id="49cee-123">需求</span><span class="sxs-lookup"><span data-stu-id="49cee-123">Requirement</span></span> | <span data-ttu-id="49cee-124">值</span><span class="sxs-lookup"><span data-stu-id="49cee-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49cee-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49cee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49cee-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49cee-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49cee-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49cee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49cee-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49cee-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="49cee-129">標頭</span><span class="sxs-lookup"><span data-stu-id="49cee-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cee-130"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="49cee-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cee-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49cee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cee-132">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="49cee-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="49cee-133">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="49cee-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="49cee-134">IMR \_ RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="49cee-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="49cee-135">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="49cee-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="49cee-136">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="49cee-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




