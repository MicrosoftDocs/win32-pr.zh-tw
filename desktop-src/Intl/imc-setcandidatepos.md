---
description: 指示 IME 視窗設定候選視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: 'IMC_SETCANDIDATEPOS 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690851"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="5d19b-104">IMC \_ SETCANDIDATEPOS 命令</span><span class="sxs-lookup"><span data-stu-id="5d19b-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="5d19b-105">指示 IME 視窗設定候選視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="5d19b-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="5d19b-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="5d19b-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="5d19b-107">參數</span><span class="sxs-lookup"><span data-stu-id="5d19b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d19b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d19b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="5d19b-109">設定為 IMC \_ SETCANDIDATEPOS。</span><span class="sxs-lookup"><span data-stu-id="5d19b-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="5d19b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d19b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5d19b-111">[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)結構的指標，其中包含候選視窗的 x 座標和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="5d19b-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="5d19b-112">應用程式應該設定此結構的 **dwIndex** 成員。</span><span class="sxs-lookup"><span data-stu-id="5d19b-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d19b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d19b-113">Return Value</span></span>

<span data-ttu-id="5d19b-114">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5d19b-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d19b-115">備註</span><span class="sxs-lookup"><span data-stu-id="5d19b-115">Remarks</span></span>

<span data-ttu-id="5d19b-116">此命令適用于單獨顯示撰寫字元的應用程式，但使用 IME 視窗顯示候選項目。</span><span class="sxs-lookup"><span data-stu-id="5d19b-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d19b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d19b-117">Requirements</span></span>



| <span data-ttu-id="5d19b-118">需求</span><span class="sxs-lookup"><span data-stu-id="5d19b-118">Requirement</span></span> | <span data-ttu-id="5d19b-119">值</span><span class="sxs-lookup"><span data-stu-id="5d19b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d19b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d19b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d19b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d19b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d19b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d19b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d19b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d19b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5d19b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5d19b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d19b-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5d19b-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d19b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d19b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d19b-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="5d19b-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="5d19b-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="5d19b-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="5d19b-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="5d19b-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="5d19b-130">**WM \_ IME \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="5d19b-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




