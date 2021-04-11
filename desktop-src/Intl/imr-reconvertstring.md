---
description: 當選取的輸入法需要字串進行漢字重漢字時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: 'IMR_RECONVERTSTRING 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849173"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="670b2-104">IMR \_ RECONVERTSTRING 通知碼</span><span class="sxs-lookup"><span data-stu-id="670b2-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="670b2-105">當選取的輸入法需要字串進行漢字重漢字時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="670b2-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="670b2-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="670b2-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="670b2-107">參數</span><span class="sxs-lookup"><span data-stu-id="670b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670b2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="670b2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="670b2-109">設定為 IMR \_ RECONVERTSTRING。</span><span class="sxs-lookup"><span data-stu-id="670b2-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="670b2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="670b2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="670b2-111">包含 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構和字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="670b2-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670b2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="670b2-112">Return Value</span></span>

<span data-ttu-id="670b2-113">傳回目前的漢字重組字串結構。</span><span class="sxs-lookup"><span data-stu-id="670b2-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="670b2-114">如果 *lParam* 設定為 **Null**，則應用程式會傳回保存結構所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="670b2-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="670b2-115">如果不成功，此命令會傳回0。</span><span class="sxs-lookup"><span data-stu-id="670b2-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="670b2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="670b2-116">Requirements</span></span>



| <span data-ttu-id="670b2-117">需求</span><span class="sxs-lookup"><span data-stu-id="670b2-117">Requirement</span></span> | <span data-ttu-id="670b2-118">值</span><span class="sxs-lookup"><span data-stu-id="670b2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670b2-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="670b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="670b2-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="670b2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="670b2-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="670b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="670b2-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="670b2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="670b2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="670b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="670b2-124"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="670b2-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670b2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="670b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670b2-126">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="670b2-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="670b2-127">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="670b2-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="670b2-128">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="670b2-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="670b2-129">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="670b2-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




