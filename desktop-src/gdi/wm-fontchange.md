---
description: 應用程式會在 \_ 變更字型資源的集區之後，將 WM FONTCHANGE 訊息傳送至系統中的所有最上層視窗。
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: 'WM_FONTCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973516"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="d63c6-103">WM \_ FONTCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="d63c6-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="d63c6-104">應用程式會在變更字型資源的集區之後，將 **WM \_ FONTCHANGE** 訊息傳送至系統中的所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="d63c6-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="d63c6-105">若要傳送此訊息，請使用下列參數呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="d63c6-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="d63c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="d63c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d63c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d63c6-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d63c6-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d63c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d63c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d63c6-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d63c6-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d63c6-111">備註</span><span class="sxs-lookup"><span data-stu-id="d63c6-111">Remarks</span></span>

<span data-ttu-id="d63c6-112">從系統新增或移除字型 (例如使用 [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) 或) [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 函式的應用程式，應該會將此訊息傳送至所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="d63c6-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="d63c6-113">若要將 **WM \_ FONTCHANGE** 訊息傳送至所有最上層視窗，應用程式可以呼叫 **SendMessage** 函式，並將 *hwnd* 參數設定為 hwnd \_ 廣播。</span><span class="sxs-lookup"><span data-stu-id="d63c6-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63c6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d63c6-114">Requirements</span></span>



| <span data-ttu-id="d63c6-115">需求</span><span class="sxs-lookup"><span data-stu-id="d63c6-115">Requirement</span></span> | <span data-ttu-id="d63c6-116">值</span><span class="sxs-lookup"><span data-stu-id="d63c6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63c6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d63c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d63c6-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63c6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d63c6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d63c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d63c6-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63c6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d63c6-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d63c6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63c6-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d63c6-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63c6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d63c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63c6-124">字型和文字總覽</span><span class="sxs-lookup"><span data-stu-id="d63c6-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="d63c6-125">字型和文字訊息</span><span class="sxs-lookup"><span data-stu-id="d63c6-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="d63c6-126">**AddFontResource**</span><span class="sxs-lookup"><span data-stu-id="d63c6-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="d63c6-127">**RemoveFontResource**</span><span class="sxs-lookup"><span data-stu-id="d63c6-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
