---
description: 指示 IME 視窗取得候選視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: 'IMC_GETCANDIDATEPOS 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992207"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="f22d6-104">IMC \_ GETCANDIDATEPOS 命令</span><span class="sxs-lookup"><span data-stu-id="f22d6-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="f22d6-105">指示 IME 視窗取得候選視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="f22d6-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="f22d6-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="f22d6-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="f22d6-107">參數</span><span class="sxs-lookup"><span data-stu-id="f22d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f22d6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f22d6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f22d6-109">設定為 IMC \_ GETCANDIDATEPOS。</span><span class="sxs-lookup"><span data-stu-id="f22d6-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="f22d6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f22d6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f22d6-111">[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)結構的指標，其中包含候選視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="f22d6-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f22d6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f22d6-112">Return Value</span></span>

<span data-ttu-id="f22d6-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f22d6-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f22d6-114">備註</span><span class="sxs-lookup"><span data-stu-id="f22d6-114">Remarks</span></span>

<span data-ttu-id="f22d6-115">因為 IME 可能會調整候選視窗的位置，應用程式會使用這個命令來取得實際的位置，以決定是否要重新放置視窗。</span><span class="sxs-lookup"><span data-stu-id="f22d6-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="f22d6-116">抓取的位置是在視窗座標中，相對於具有目前輸入焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="f22d6-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="f22d6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f22d6-117">Requirements</span></span>



| <span data-ttu-id="f22d6-118">需求</span><span class="sxs-lookup"><span data-stu-id="f22d6-118">Requirement</span></span> | <span data-ttu-id="f22d6-119">值</span><span class="sxs-lookup"><span data-stu-id="f22d6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22d6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f22d6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f22d6-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f22d6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f22d6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f22d6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f22d6-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f22d6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f22d6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f22d6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f22d6-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f22d6-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22d6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f22d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22d6-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="f22d6-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f22d6-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="f22d6-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f22d6-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="f22d6-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




