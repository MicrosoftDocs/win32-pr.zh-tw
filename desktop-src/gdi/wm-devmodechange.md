---
description: '\_只要使用者變更裝置模式設定，就會將 WM DEVMODECHANGE 訊息傳送至所有最上層視窗。'
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: 'WM_DEVMODECHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973517"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="56fc0-103">WM \_ DEVMODECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="56fc0-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="56fc0-104">只要使用者變更裝置模式設定，就會將 **WM \_ DEVMODECHANGE** 訊息傳送至所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="56fc0-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="56fc0-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="56fc0-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="56fc0-106">參數</span><span class="sxs-lookup"><span data-stu-id="56fc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56fc0-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="56fc0-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="56fc0-108">視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="56fc0-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="56fc0-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="56fc0-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="56fc0-110">WM \_ DEVMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="56fc0-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="56fc0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56fc0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56fc0-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="56fc0-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="56fc0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56fc0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56fc0-114">指定裝置名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="56fc0-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56fc0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="56fc0-115">Return value</span></span>

<span data-ttu-id="56fc0-116">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="56fc0-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="56fc0-117">備註</span><span class="sxs-lookup"><span data-stu-id="56fc0-117">Remarks</span></span>

<span data-ttu-id="56fc0-118">此訊息無法直接傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="56fc0-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="56fc0-119">若要將 **WM \_ DEVMODECHANGE** 訊息傳送至所有最上層視窗，請使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式並將 *hwnd* 參數設定為 hwnd \_ 廣播。</span><span class="sxs-lookup"><span data-stu-id="56fc0-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="56fc0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="56fc0-120">Requirements</span></span>



| <span data-ttu-id="56fc0-121">需求</span><span class="sxs-lookup"><span data-stu-id="56fc0-121">Requirement</span></span> | <span data-ttu-id="56fc0-122">值</span><span class="sxs-lookup"><span data-stu-id="56fc0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56fc0-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56fc0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56fc0-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56fc0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="56fc0-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56fc0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56fc0-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56fc0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56fc0-127">標頭</span><span class="sxs-lookup"><span data-stu-id="56fc0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="56fc0-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="56fc0-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56fc0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56fc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fc0-130">裝置內容總覽</span><span class="sxs-lookup"><span data-stu-id="56fc0-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="56fc0-131">裝置內容訊息</span><span class="sxs-lookup"><span data-stu-id="56fc0-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 
