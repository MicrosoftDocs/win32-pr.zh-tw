---
description: 當輸入內容的句子模式更新時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 72455193-cd17-45f8-b19c-a1f735ff81bf
title: 'IMN_SETSENTENCEMODE 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0130c5b3d7284112e64cca698b358650f51f3642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975081"
---
# <a name="imn_setsentencemode-notification-code"></a><span data-ttu-id="48754-104">IMN \_ SETSENTENCEMODE 通知碼</span><span class="sxs-lookup"><span data-stu-id="48754-104">IMN\_SETSENTENCEMODE notification code</span></span>

<span data-ttu-id="48754-105">當輸入內容的句子模式更新時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="48754-105">Notifies an application when the sentence mode of the input context is updated.</span></span> <span data-ttu-id="48754-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="48754-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETSENTENCEMODE
```



## <a name="parameters"></a><span data-ttu-id="48754-107">參數</span><span class="sxs-lookup"><span data-stu-id="48754-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48754-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="48754-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="48754-109">設定為 IMN \_ SETSENTENCEMODE。</span><span class="sxs-lookup"><span data-stu-id="48754-109">Set to IMN\_SETSENTENCEMODE.</span></span>

</dd> <dt>

<span data-ttu-id="48754-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="48754-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="48754-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="48754-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48754-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="48754-112">Return Value</span></span>

<span data-ttu-id="48754-113">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="48754-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48754-114">備註</span><span class="sxs-lookup"><span data-stu-id="48754-114">Remarks</span></span>

<span data-ttu-id="48754-115">應用程式可以使用 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 函數來取得句子模式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="48754-115">The application can get information about the sentence mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="48754-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="48754-116">Requirements</span></span>



| <span data-ttu-id="48754-117">需求</span><span class="sxs-lookup"><span data-stu-id="48754-117">Requirement</span></span> | <span data-ttu-id="48754-118">值</span><span class="sxs-lookup"><span data-stu-id="48754-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48754-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48754-119">Minimum supported client</span></span><br/> | <span data-ttu-id="48754-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48754-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="48754-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48754-121">Minimum supported server</span></span><br/> | <span data-ttu-id="48754-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48754-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="48754-123">標頭</span><span class="sxs-lookup"><span data-stu-id="48754-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="48754-124"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="48754-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48754-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48754-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48754-126">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="48754-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="48754-127">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="48754-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="48754-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="48754-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="48754-129">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="48754-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




