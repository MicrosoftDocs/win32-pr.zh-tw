---
description: IsWindowRedirectedForPrint 函式會判斷指定的視窗目前是否重新導向以進行列印。
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983895"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="2c8e8-103">IsWindowRedirectedForPrint 函式</span><span class="sxs-lookup"><span data-stu-id="2c8e8-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="2c8e8-104">**IsWindowRedirectedForPrint** 函式會判斷指定的視窗目前是否重新導向以進行列印。</span><span class="sxs-lookup"><span data-stu-id="2c8e8-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c8e8-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="2c8e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c8e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8e8-107">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c8e8-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8e8-108">視窗控制代碼。</span><span class="sxs-lookup"><span data-stu-id="2c8e8-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8e8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c8e8-109">Return value</span></span>

<span data-ttu-id="2c8e8-110">如果視窗目前重新導向以進行列印，則函式會傳回非零值。否則，它會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2c8e8-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8e8-111">備註</span><span class="sxs-lookup"><span data-stu-id="2c8e8-111">Remarks</span></span>

<span data-ttu-id="2c8e8-112">當視窗處理 [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)的呼叫時，會將視窗重新導向以進行列印。</span><span class="sxs-lookup"><span data-stu-id="2c8e8-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="2c8e8-113">在 **PrintWindow** 的呼叫中，視窗會將其內容轉譯為螢幕上的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2c8e8-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="2c8e8-114">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="2c8e8-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8e8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c8e8-115">Requirements</span></span>



| <span data-ttu-id="2c8e8-116">需求</span><span class="sxs-lookup"><span data-stu-id="2c8e8-116">Requirement</span></span> | <span data-ttu-id="2c8e8-117">值</span><span class="sxs-lookup"><span data-stu-id="2c8e8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8e8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c8e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8e8-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c8e8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c8e8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c8e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8e8-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c8e8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c8e8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8e8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8e8-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8e8-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8e8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c8e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8e8-125">**PrintWindow**</span><span class="sxs-lookup"><span data-stu-id="2c8e8-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="2c8e8-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="2c8e8-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="2c8e8-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="2c8e8-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="2c8e8-128">**WM \_ 列印**</span><span class="sxs-lookup"><span data-stu-id="2c8e8-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="2c8e8-129">**WM \_ PRINTCLIENT**</span><span class="sxs-lookup"><span data-stu-id="2c8e8-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

