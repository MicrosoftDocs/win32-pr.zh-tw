---
description: 取消註冊 LinkWindow RegisterClass 所註冊的視窗類別 \_ 。
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973381"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="c2486-103">LinkWindow \_ UnregisterClass 函式</span><span class="sxs-lookup"><span data-stu-id="c2486-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="c2486-104">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="c2486-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c2486-105">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c2486-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c2486-106">取消註冊 [**LinkWindow \_ RegisterClass**](linkwindow-registerclass.md)所註冊的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="c2486-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2486-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2486-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="c2486-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2486-108">Parameters</span></span>

<span data-ttu-id="c2486-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="c2486-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2486-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2486-110">Return value</span></span>

<span data-ttu-id="c2486-111">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="c2486-111">Type: **BOOL**</span></span>

<span data-ttu-id="c2486-112">如果作業成功，則傳回 **TRUE** ;否則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c2486-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2486-113">備註</span><span class="sxs-lookup"><span data-stu-id="c2486-113">Remarks</span></span>

<span data-ttu-id="c2486-114">此函式沒有相關聯的標頭或程式庫檔案，因此必須由序數值來呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2486-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="c2486-115">使用 Shell32.dll 的 DLL 名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="c2486-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="c2486-116">然後使用該模組控制碼呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，並使用序號259來使用此函數。</span><span class="sxs-lookup"><span data-stu-id="c2486-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2486-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2486-117">Requirements</span></span>



| <span data-ttu-id="c2486-118">需求</span><span class="sxs-lookup"><span data-stu-id="c2486-118">Requirement</span></span> | <span data-ttu-id="c2486-119">值</span><span class="sxs-lookup"><span data-stu-id="c2486-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2486-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2486-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2486-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2486-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2486-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2486-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2486-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2486-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c2486-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c2486-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2486-125"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c2486-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2486-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2486-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2486-127">SysLink 控制項總覽</span><span class="sxs-lookup"><span data-stu-id="c2486-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
