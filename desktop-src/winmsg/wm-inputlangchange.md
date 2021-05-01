---
description: 在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。 您應該進行任何應用程式專屬的設定，並將訊息傳遞至 DefWindowProc 函式，此函式會將訊息傳遞給所有的第一層子視窗。
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: 'WM_INPUTLANGCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332403"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="5351c-104">WM \_ INPUTLANGCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="5351c-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="5351c-105">在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。</span><span class="sxs-lookup"><span data-stu-id="5351c-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="5351c-106">您應該進行任何應用程式專屬的設定，並將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，此函式會將訊息傳遞給所有的第一層子視窗。</span><span class="sxs-lookup"><span data-stu-id="5351c-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="5351c-107">這些子視窗可以將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓它將訊息傳遞給其子視窗，依此類推。</span><span class="sxs-lookup"><span data-stu-id="5351c-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="5351c-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="5351c-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="5351c-109">參數</span><span class="sxs-lookup"><span data-stu-id="5351c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5351c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5351c-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="5351c-111">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="5351c-111">Type: **WPARAM**</span></span>

<span data-ttu-id="5351c-112">新地區設定的 [字碼頁](../Intl/code-pages.md) 。</span><span class="sxs-lookup"><span data-stu-id="5351c-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="5351c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5351c-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="5351c-114">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="5351c-114">Type: **LPARAM**</span></span>

<span data-ttu-id="5351c-115">**HKL** 輸入地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="5351c-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="5351c-116">如需詳細資訊，請參閱 [語言、地區設定和鍵盤配置](../inputdev/about-keyboard-input.md)。</span><span class="sxs-lookup"><span data-stu-id="5351c-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5351c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5351c-117">Return value</span></span>

<span data-ttu-id="5351c-118">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5351c-118">Type: **LRESULT**</span></span>

<span data-ttu-id="5351c-119">如果應用程式處理此訊息，則應該傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5351c-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5351c-120">備註</span><span class="sxs-lookup"><span data-stu-id="5351c-120">Remarks</span></span>

<span data-ttu-id="5351c-121">您可以透過[LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename)函式來取得鍵盤[地區設定名稱](../Intl/locale-names.md)。</span><span class="sxs-lookup"><span data-stu-id="5351c-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="5351c-122">您可以使用地區設定名稱來使用 [新式地區設定函數](/windows/win32/intl/calling-the--locale-name--functions)：</span><span class="sxs-lookup"><span data-stu-id="5351c-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="5351c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5351c-123">Requirements</span></span>

| <span data-ttu-id="5351c-124">需求</span><span class="sxs-lookup"><span data-stu-id="5351c-124">Requirement</span></span> | <span data-ttu-id="5351c-125">值</span><span class="sxs-lookup"><span data-stu-id="5351c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5351c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5351c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5351c-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5351c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5351c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5351c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5351c-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5351c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5351c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5351c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5351c-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5351c-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="5351c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5351c-132">See also</span></span>

<span data-ttu-id="5351c-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="5351c-133">**Reference**</span></span>

- [<span data-ttu-id="5351c-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5351c-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="5351c-135">**WM \_ INPUTLANGCHANGEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="5351c-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="5351c-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="5351c-136">**Conceptual**</span></span>

- [<span data-ttu-id="5351c-137">Windows</span><span class="sxs-lookup"><span data-stu-id="5351c-137">Windows</span></span>](windows.md) 
