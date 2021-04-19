---
description: 當輸入內容的轉換模式更新時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: 'IMN_SETCONVERSIONMODE 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989980"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="cada7-104">IMN \_ SETCONVERSIONMODE 通知碼</span><span class="sxs-lookup"><span data-stu-id="cada7-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="cada7-105">當輸入內容的轉換模式更新時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="cada7-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="cada7-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cada7-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="cada7-107">參數</span><span class="sxs-lookup"><span data-stu-id="cada7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cada7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="cada7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="cada7-109">設定為 IMN \_ SETCONVERSIONMODE。</span><span class="sxs-lookup"><span data-stu-id="cada7-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="cada7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="cada7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="cada7-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="cada7-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cada7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cada7-112">Return Value</span></span>

<span data-ttu-id="cada7-113">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="cada7-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cada7-114">備註</span><span class="sxs-lookup"><span data-stu-id="cada7-114">Remarks</span></span>

<span data-ttu-id="cada7-115">應用程式可以使用 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 函數來取得轉換模式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cada7-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cada7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cada7-116">Requirements</span></span>



| <span data-ttu-id="cada7-117">需求</span><span class="sxs-lookup"><span data-stu-id="cada7-117">Requirement</span></span> | <span data-ttu-id="cada7-118">值</span><span class="sxs-lookup"><span data-stu-id="cada7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cada7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cada7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cada7-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cada7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cada7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cada7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cada7-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cada7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cada7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cada7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cada7-124"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cada7-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cada7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cada7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cada7-126">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="cada7-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cada7-127">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="cada7-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="cada7-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="cada7-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="cada7-129">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="cada7-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




