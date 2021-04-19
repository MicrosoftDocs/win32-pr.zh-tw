---
description: 事件處理常式原型函式用於所有處理 Winlogon 通知事件的函式。
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: 事件處理常式函式原型回呼函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978334"
---
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="5fb1e-103">事件處理常式函式原型回呼函數</span><span class="sxs-lookup"><span data-stu-id="5fb1e-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="5fb1e-104">\[從 Windows Server 2008 和 Windows Vista 起，無法再使用事件處理常式原型函式。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5fb1e-105">\]</span><span class="sxs-lookup"><span data-stu-id="5fb1e-105">\]</span></span>

<span data-ttu-id="5fb1e-106">事件處理常式原型函式用於所有處理 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 通知事件的函式。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="5fb1e-107">函式名稱（以預留位置 *事件 \_ 處理常式函式 \_ \_ 名稱* 表示）通常會反映函式處理的事件名稱。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="5fb1e-108">例如，處理登入事件的函式可能會命名為： **WLEventLogon**。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb1e-109">語法</span><span class="sxs-lookup"><span data-stu-id="5fb1e-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5fb1e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5fb1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb1e-111">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fb1e-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb1e-112">[**WLX \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info)結構的指標，其中包含事件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb1e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fb1e-113">Return value</span></span>

<span data-ttu-id="5fb1e-114">這個回呼函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb1e-115">備註</span><span class="sxs-lookup"><span data-stu-id="5fb1e-115">Remarks</span></span>

<span data-ttu-id="5fb1e-116">如果您的事件處理常式需要建立子進程，它應該呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函數。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="5fb1e-117">否則，就會在 Winlogon 桌面上建立新的進程，而不是使用者的桌面。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="5fb1e-118">範例</span><span class="sxs-lookup"><span data-stu-id="5fb1e-118">Examples</span></span>

<span data-ttu-id="5fb1e-119">下列範例會示範如何執行 Winlogon 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="5fb1e-120">為了簡單起見，系統只會顯示登入和登出事件處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="5fb1e-121">您可以用完全相同的方式來執行其餘事件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="5fb1e-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a><span data-ttu-id="5fb1e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fb1e-122">Requirements</span></span>



| <span data-ttu-id="5fb1e-123">需求</span><span class="sxs-lookup"><span data-stu-id="5fb1e-123">Requirement</span></span> | <span data-ttu-id="5fb1e-124">值</span><span class="sxs-lookup"><span data-stu-id="5fb1e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5fb1e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fb1e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5fb1e-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fb1e-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5fb1e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fb1e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5fb1e-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fb1e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5fb1e-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5fb1e-129">End of client support</span></span><br/>    | <span data-ttu-id="5fb1e-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5fb1e-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="5fb1e-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5fb1e-131">End of server support</span></span><br/>    | <span data-ttu-id="5fb1e-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fb1e-132">Windows Server 2003</span></span><br/>                       |



 

