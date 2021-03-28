---
description: 傳送至已使用 Windows 說明起始定型卡的應用程式。
title: 'WM_TCARD 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192672"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="a031e-103">WM \_ TCARD 訊息</span><span class="sxs-lookup"><span data-stu-id="a031e-103">WM\_TCARD message</span></span>

<span data-ttu-id="a031e-104">傳送至已使用 Windows 說明起始定型卡的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a031e-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="a031e-105">當使用者按一下 [authorable] 按鈕時，訊息會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="a031e-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="a031e-106">應用程式會在對 WinHelp 函式的 \_ 呼叫中指定 HELP TCARD 命令，以[](/windows/desktop/api/Winuser/nf-winuser-winhelpa)起始定型卡。</span><span class="sxs-lookup"><span data-stu-id="a031e-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="a031e-107">參數</span><span class="sxs-lookup"><span data-stu-id="a031e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a031e-108">*idAction*</span><span class="sxs-lookup"><span data-stu-id="a031e-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="a031e-109">值，指出使用者已採取的動作。</span><span class="sxs-lookup"><span data-stu-id="a031e-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="a031e-110">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a031e-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="a031e-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span><span class="sxs-lookup"><span data-stu-id="a031e-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-112">使用者按一下 [authorable **中止** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="a031e-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="a031e-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-114">使用者按一下 [authorable **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="a031e-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span><span class="sxs-lookup"><span data-stu-id="a031e-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-116">使用者已關閉訓練卡。</span><span class="sxs-lookup"><span data-stu-id="a031e-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="a031e-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span><span class="sxs-lookup"><span data-stu-id="a031e-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-118">使用者按一下 [authorable **] 視窗的** [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="a031e-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span><span class="sxs-lookup"><span data-stu-id="a031e-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-120">使用者按一下 authorable [ **略** 過] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="a031e-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span><span class="sxs-lookup"><span data-stu-id="a031e-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-122">使用者按一下 [authorable **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="a031e-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span><span class="sxs-lookup"><span data-stu-id="a031e-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-124">使用者按一下 authorable **No** button。</span><span class="sxs-lookup"><span data-stu-id="a031e-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="a031e-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span><span class="sxs-lookup"><span data-stu-id="a031e-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-126">使用者按一下 authorable **重試** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="a031e-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**協助 \_ TCARD \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a031e-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-128">使用者按一下 [authorable] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-128">The user clicked an authorable button.</span></span> <span data-ttu-id="a031e-129">*DwActionData* 參數包含由說明作者指定的長整數。</span><span class="sxs-lookup"><span data-stu-id="a031e-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="a031e-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**協助 \_ TCARD \_ 其他 \_ 呼叫者**</span><span class="sxs-lookup"><span data-stu-id="a031e-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-131">另一個應用程式已要求定型卡。</span><span class="sxs-lookup"><span data-stu-id="a031e-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="a031e-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span><span class="sxs-lookup"><span data-stu-id="a031e-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="a031e-133">使用者按一下 [authorable **是]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a031e-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a031e-134">*dwActionData*</span><span class="sxs-lookup"><span data-stu-id="a031e-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="a031e-135">如果 *idAction* 指定 help \_ TCARD \_ 資料，則此參數是由說明作者指定的 **長整數** 。</span><span class="sxs-lookup"><span data-stu-id="a031e-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="a031e-136">否則，此參數為零。</span><span class="sxs-lookup"><span data-stu-id="a031e-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a031e-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="a031e-137">Return value</span></span>

<span data-ttu-id="a031e-138">傳回值會被忽略;使用零。</span><span class="sxs-lookup"><span data-stu-id="a031e-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a031e-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="a031e-139">Requirements</span></span>



| <span data-ttu-id="a031e-140">需求</span><span class="sxs-lookup"><span data-stu-id="a031e-140">Requirement</span></span> | <span data-ttu-id="a031e-141">值</span><span class="sxs-lookup"><span data-stu-id="a031e-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a031e-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a031e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a031e-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a031e-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a031e-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a031e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a031e-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a031e-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a031e-146">標頭</span><span class="sxs-lookup"><span data-stu-id="a031e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a031e-147"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="a031e-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 




