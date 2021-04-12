---
description: 指示 IME 視窗取出用來在組合視窗中顯示中繼字元的邏輯字型。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: 'IMC_GETCOMPOSITIONFONT 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191506"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="f355e-104">IMC \_ GETCOMPOSITIONFONT 命令</span><span class="sxs-lookup"><span data-stu-id="f355e-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="f355e-105">指示 IME 視窗取出用來在組合視窗中顯示中繼字元的邏輯字型。</span><span class="sxs-lookup"><span data-stu-id="f355e-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="f355e-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="f355e-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="f355e-107">參數</span><span class="sxs-lookup"><span data-stu-id="f355e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f355e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f355e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f355e-109">設定為 IMC \_ GETCOMPOSITIONFONT。</span><span class="sxs-lookup"><span data-stu-id="f355e-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="f355e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f355e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f355e-111">[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，此結構會接收邏輯字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f355e-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f355e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f355e-112">Return Value</span></span>

<span data-ttu-id="f355e-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f355e-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f355e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f355e-114">Requirements</span></span>



| <span data-ttu-id="f355e-115">需求</span><span class="sxs-lookup"><span data-stu-id="f355e-115">Requirement</span></span> | <span data-ttu-id="f355e-116">值</span><span class="sxs-lookup"><span data-stu-id="f355e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f355e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f355e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f355e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f355e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f355e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f355e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f355e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f355e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f355e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f355e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f355e-122"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f355e-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f355e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f355e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f355e-124">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="f355e-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f355e-125">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="f355e-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 
