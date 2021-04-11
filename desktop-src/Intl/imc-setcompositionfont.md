---
description: 指示 IME 視窗指定要在組合視窗中用來顯示中繼字元的邏輯字型。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: 'IMC_SETCOMPOSITIONFONT 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848193"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="b26c6-104">IMC \_ SETCOMPOSITIONFONT 命令</span><span class="sxs-lookup"><span data-stu-id="b26c6-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="b26c6-105">指示 IME 視窗指定要在組合視窗中用來顯示中繼字元的邏輯字型。</span><span class="sxs-lookup"><span data-stu-id="b26c6-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="b26c6-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="b26c6-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="b26c6-107">參數</span><span class="sxs-lookup"><span data-stu-id="b26c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b26c6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b26c6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b26c6-109">設定為 IMC \_ SETCOMPOSITIONFONT。</span><span class="sxs-lookup"><span data-stu-id="b26c6-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="b26c6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b26c6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b26c6-111">[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，其中包含邏輯字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b26c6-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b26c6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b26c6-112">Return Value</span></span>

<span data-ttu-id="b26c6-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="b26c6-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b26c6-114">備註</span><span class="sxs-lookup"><span data-stu-id="b26c6-114">Remarks</span></span>

<span data-ttu-id="b26c6-115">處理此命令時，IME 視窗會變更輸入內容中目前所選取的字型。</span><span class="sxs-lookup"><span data-stu-id="b26c6-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="b26c6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b26c6-116">Requirements</span></span>



| <span data-ttu-id="b26c6-117">需求</span><span class="sxs-lookup"><span data-stu-id="b26c6-117">Requirement</span></span> | <span data-ttu-id="b26c6-118">值</span><span class="sxs-lookup"><span data-stu-id="b26c6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b26c6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b26c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b26c6-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b26c6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b26c6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b26c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b26c6-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b26c6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b26c6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b26c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b26c6-124"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b26c6-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b26c6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b26c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b26c6-126">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="b26c6-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b26c6-127">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="b26c6-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b26c6-128">**WM \_ IME \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="b26c6-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
