---
description: 當 SystemParametersInfo 函式變更整個系統的設定或原則設定變更時，傳送至所有最上層視窗的訊息。
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: 'WM_SETTINGCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194955"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="e5362-103">WM \_ SETTINGCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="e5362-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="e5362-104">當 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式變更整個系統的設定或原則設定變更時，傳送至所有最上層視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="e5362-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="e5362-105">應用程式應該會在對系統參數進行變更時，將 **WM \_ SETTINGCHANGE** 傳送至所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="e5362-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="e5362-106"> (無法直接將此訊息傳送至視窗。 ) 若要將 **WM \_ SETTINGCHANGE** 訊息傳送至所有最上層視窗，請使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式並將 *hwnd* 參數設定為 **hwnd \_ 廣播**。</span><span class="sxs-lookup"><span data-stu-id="e5362-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="e5362-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e5362-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="e5362-108">參數</span><span class="sxs-lookup"><span data-stu-id="e5362-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5362-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5362-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5362-110">當系統傳送此訊息作為 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)呼叫的結果時， *wParam* 參數是傳遞給 **SystemParametersInfo** 函數的 *uiAction* 參數值。</span><span class="sxs-lookup"><span data-stu-id="e5362-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="e5362-111">如需值的清單，請參閱 **SystemParametersInfo**。</span><span class="sxs-lookup"><span data-stu-id="e5362-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="e5362-112">當系統由於原則設定變更而傳送此訊息時，此參數會指出已套用的原則類型。</span><span class="sxs-lookup"><span data-stu-id="e5362-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="e5362-113">如果套用了電腦原則，則此值為1，如果套用了使用者原則，則為零。</span><span class="sxs-lookup"><span data-stu-id="e5362-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="e5362-114">當系統因地區設定變更而傳送此訊息時，此參數為零。</span><span class="sxs-lookup"><span data-stu-id="e5362-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="e5362-115">當應用程式傳送此訊息時，此參數必須為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5362-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e5362-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5362-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5362-117">當系統傳送此訊息作為 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 呼叫的結果時， *lParam* 是指向字串的指標，指出包含已變更之系統參數的區域。</span><span class="sxs-lookup"><span data-stu-id="e5362-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="e5362-118">此參數通常不會指出哪些特定的系統參數已變更。</span><span class="sxs-lookup"><span data-stu-id="e5362-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="e5362-119"> (請注意，有些應用程式會傳送此訊息，並將 *lParam* 設定為 **Null**。 ) 一般而言，當您收到此訊息時，您應該檢查並重載您的應用程式所使用的任何系統參數設定。</span><span class="sxs-lookup"><span data-stu-id="e5362-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="e5362-120">這個字串可以是登錄機碼的名稱或 Win.ini 檔案中區段的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5362-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="e5362-121">當字串是登錄名稱時，通常只會指出登錄中的分葉節點，而不是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e5362-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="e5362-122">當系統由於原則設定變更而傳送此訊息時，此參數會指向字串 "Policy"。</span><span class="sxs-lookup"><span data-stu-id="e5362-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="e5362-123">當系統因地區設定的變更而傳送此訊息時，此參數會指向字串 "國際"。</span><span class="sxs-lookup"><span data-stu-id="e5362-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="e5362-124">若要對系統或使用者的環境變數產生變更，請將 *lParam* 設定為字串 "環境" 的訊息廣播。</span><span class="sxs-lookup"><span data-stu-id="e5362-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5362-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5362-125">Return value</span></span>

<span data-ttu-id="e5362-126">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e5362-126">Type: **LRESULT**</span></span>

<span data-ttu-id="e5362-127">如果您處理此訊息，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="e5362-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5362-128">備註</span><span class="sxs-lookup"><span data-stu-id="e5362-128">Remarks</span></span>

<span data-ttu-id="e5362-129">*LParam* 參數會指出已變更的系統計量，例如，如果已切換 ConvertibleSlateMode 指標，則為 "ConvertibleSlateMode"，如果停駐指標已切換，則為 "SystemDockMode"。</span><span class="sxs-lookup"><span data-stu-id="e5362-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5362-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5362-130">Requirements</span></span>



| <span data-ttu-id="e5362-131">需求</span><span class="sxs-lookup"><span data-stu-id="e5362-131">Requirement</span></span> | <span data-ttu-id="e5362-132">值</span><span class="sxs-lookup"><span data-stu-id="e5362-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5362-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5362-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e5362-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5362-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e5362-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5362-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e5362-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5362-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5362-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e5362-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5362-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e5362-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5362-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5362-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5362-140">原則事件</span><span class="sxs-lookup"><span data-stu-id="e5362-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="e5362-141">**SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="e5362-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="e5362-142">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="e5362-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
