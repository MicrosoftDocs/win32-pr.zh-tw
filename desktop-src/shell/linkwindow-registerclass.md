---
description: 註冊視窗類別，讓 SysLink 通用控制項可以在視窗中使用。
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973384"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="8f9fd-103">LinkWindow \_ RegisterClass 函式</span><span class="sxs-lookup"><span data-stu-id="8f9fd-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="8f9fd-104">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="8f9fd-105">它可能會在後續版本的 Windows 中改變或無法使用。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="8f9fd-106">請改用 [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) 。\]</span><span class="sxs-lookup"><span data-stu-id="8f9fd-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="8f9fd-107">註冊視窗類別，讓 [SysLink](../controls/syslink-overview.md) 通用控制項可以在視窗中使用。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9fd-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f9fd-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="8f9fd-109">參數</span><span class="sxs-lookup"><span data-stu-id="8f9fd-109">Parameters</span></span>

<span data-ttu-id="8f9fd-110">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f9fd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f9fd-111">Return value</span></span>

<span data-ttu-id="8f9fd-112">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="8f9fd-112">Type: **BOOL**</span></span>

<span data-ttu-id="8f9fd-113">如果註冊成功，則傳回 **TRUE** ;否則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9fd-114">備註</span><span class="sxs-lookup"><span data-stu-id="8f9fd-114">Remarks</span></span>

<span data-ttu-id="8f9fd-115">此函式沒有相關聯的標頭或程式庫檔案，因此必須由序數值來呼叫。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="8f9fd-116">使用 Shell32.dll 的 DLL 名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="8f9fd-117">然後使用該模組控制碼呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，並使用序號258來使用此函數。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="8f9fd-118">使用 [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) 在使用後取消註冊類別。</span><span class="sxs-lookup"><span data-stu-id="8f9fd-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9fd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f9fd-119">Requirements</span></span>



| <span data-ttu-id="8f9fd-120">需求</span><span class="sxs-lookup"><span data-stu-id="8f9fd-120">Requirement</span></span> | <span data-ttu-id="8f9fd-121">值</span><span class="sxs-lookup"><span data-stu-id="8f9fd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9fd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f9fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9fd-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f9fd-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f9fd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f9fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9fd-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f9fd-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8f9fd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9fd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9fd-127"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8f9fd-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9fd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f9fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9fd-129">SysLink 控制項總覽</span><span class="sxs-lookup"><span data-stu-id="8f9fd-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
