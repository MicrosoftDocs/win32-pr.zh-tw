---
description: 應用程式會在對 \_ WIN.INI 檔案進行變更之後，將 WM WININICHANGE 訊息傳送至所有最上層視窗。 SystemParametersInfo 函式會在應用程式使用函式來變更 WIN.INI 中的設定之後傳送此訊息。
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: 'WM_WININICHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943389"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="e3866-104">WM \_ WININICHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="e3866-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="e3866-105">應用程式會在對 WIN.INI 檔案進行變更之後，將 **WM \_ WININICHANGE** 訊息傳送至所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="e3866-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="e3866-106">[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)函式會在應用程式使用函式來變更 WIN.INI 中的設定之後傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e3866-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="e3866-107">只有在與舊版系統相容時，才會提供 **WM \_ WININICHANGE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="e3866-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="e3866-108">應用程式應該使用 [**WM \_ SETTINGCHANGE**](wm-settingchange.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="e3866-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="e3866-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e3866-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="e3866-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3866-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3866-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3866-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3866-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e3866-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e3866-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3866-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3866-114">字串的指標，其中包含已變更之系統參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3866-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="e3866-115">例如，這個字串可以是登錄機碼的名稱或 Win.ini 檔中區段的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3866-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="e3866-116">此參數在判斷哪些系統參數變更時特別有用。</span><span class="sxs-lookup"><span data-stu-id="e3866-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="e3866-117">例如，當字串是登錄名稱時，通常只會指出登錄中的分葉節點，而不是整個路徑。</span><span class="sxs-lookup"><span data-stu-id="e3866-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="e3866-118">此外，某些應用程式會傳送此訊息，並將 *lParam* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e3866-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="e3866-119">一般來說，當您收到此訊息時，您應該檢查並重載您的應用程式所使用的任何系統參數設定。</span><span class="sxs-lookup"><span data-stu-id="e3866-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3866-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3866-120">Return value</span></span>

<span data-ttu-id="e3866-121">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3866-121">Type: **LRESULT**</span></span>

<span data-ttu-id="e3866-122">如果您處理此訊息，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="e3866-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3866-123">備註</span><span class="sxs-lookup"><span data-stu-id="e3866-123">Remarks</span></span>

<span data-ttu-id="e3866-124">若要將 **WM \_ WININICHANGE** 訊息傳送至所有最上層視窗，請使用 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式並將 *hwnd* 參數設定為 **hwnd \_ 廣播**。</span><span class="sxs-lookup"><span data-stu-id="e3866-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="e3866-125">呼叫變更 WIN.INI 的函式，可能會改為對應至登錄。</span><span class="sxs-lookup"><span data-stu-id="e3866-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="e3866-126">當 WIN.INI，且變更的區段在登錄中的下列機碼下指定時，就會發生此對應：</span><span class="sxs-lookup"><span data-stu-id="e3866-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="e3866-127">**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="e3866-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="e3866-128">儲存位置的變更不會影響此訊息的行為。</span><span class="sxs-lookup"><span data-stu-id="e3866-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3866-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3866-129">Requirements</span></span>



| <span data-ttu-id="e3866-130">需求</span><span class="sxs-lookup"><span data-stu-id="e3866-130">Requirement</span></span> | <span data-ttu-id="e3866-131">值</span><span class="sxs-lookup"><span data-stu-id="e3866-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3866-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3866-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e3866-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3866-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e3866-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3866-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e3866-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3866-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3866-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e3866-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3866-137"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e3866-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3866-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3866-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3866-139">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="e3866-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
