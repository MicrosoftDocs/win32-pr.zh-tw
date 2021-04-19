---
description: 當選取的輸入法需要組合字元串中字元座標的相關資訊時，就會通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: 'IMR_QUERYCHARPOSITION 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988780"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="04f76-104">IMR \_ QUERYCHARPOSITION 通知碼</span><span class="sxs-lookup"><span data-stu-id="04f76-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="04f76-105">當選取的輸入法需要組合字元串中字元座標的相關資訊時，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="04f76-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="04f76-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="04f76-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="04f76-107">參數</span><span class="sxs-lookup"><span data-stu-id="04f76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f76-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="04f76-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="04f76-109">設定為 IMR \_ QUERYCHARPOSITION。</span><span class="sxs-lookup"><span data-stu-id="04f76-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="04f76-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="04f76-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="04f76-111">[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)結構的指標，其中包含字元在組合視窗中的位置。</span><span class="sxs-lookup"><span data-stu-id="04f76-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f76-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="04f76-112">Return Value</span></span>

<span data-ttu-id="04f76-113">如果應用程式填滿 [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) 結構，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="04f76-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="04f76-114">否則，此命令會傳回0。</span><span class="sxs-lookup"><span data-stu-id="04f76-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f76-115">備註</span><span class="sxs-lookup"><span data-stu-id="04f76-115">Remarks</span></span>

<span data-ttu-id="04f76-116">繪製組合字元串本身的應用程式（而不是依賴 IME）必須負責填入 [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) 結構的所有成員。</span><span class="sxs-lookup"><span data-stu-id="04f76-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="04f76-117">否則，應用程式應該將命令傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 或 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) （如果它有自己的輸入法使用者介面視窗）。</span><span class="sxs-lookup"><span data-stu-id="04f76-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f76-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="04f76-118">Requirements</span></span>



| <span data-ttu-id="04f76-119">需求</span><span class="sxs-lookup"><span data-stu-id="04f76-119">Requirement</span></span> | <span data-ttu-id="04f76-120">值</span><span class="sxs-lookup"><span data-stu-id="04f76-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f76-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04f76-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04f76-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04f76-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04f76-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04f76-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04f76-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04f76-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04f76-125">標頭</span><span class="sxs-lookup"><span data-stu-id="04f76-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f76-126"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="04f76-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f76-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04f76-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f76-128">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="04f76-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="04f76-129">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="04f76-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="04f76-130">**IMECHARPOSITION**</span><span class="sxs-lookup"><span data-stu-id="04f76-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="04f76-131">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="04f76-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="04f76-132">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="04f76-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 
