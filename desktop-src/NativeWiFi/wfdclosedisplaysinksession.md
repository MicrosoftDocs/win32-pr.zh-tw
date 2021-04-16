---
description: 清除目前開啟的會話或目前開啟的會話的狀態。
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: 'WFDDisplaySinkCloseSession 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512768"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="b8bc8-103">WFDDisplaySinkCloseSession 函式</span><span class="sxs-lookup"><span data-stu-id="b8bc8-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="b8bc8-104">清除目前開啟的會話或目前開啟的會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8bc8-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bc8-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8bc8-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="b8bc8-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8bc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bc8-107">*hSessionHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8bc8-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8bc8-108">透過最新的 [**WFD \_ 顯示接收 \_ \_ 通知 \_ 回呼回呼**](wfd-display-sink-notification-callback.md) 的控制碼，其中包含一個。</span><span class="sxs-lookup"><span data-stu-id="b8bc8-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bc8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8bc8-109">Return value</span></span>

<span data-ttu-id="b8bc8-110">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="b8bc8-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8bc8-111">備註</span><span class="sxs-lookup"><span data-stu-id="b8bc8-111">Remarks</span></span>

<span data-ttu-id="b8bc8-112">基於任何原因，您的應用程式可以呼叫此函式來終止 Miracast 會話。</span><span class="sxs-lookup"><span data-stu-id="b8bc8-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="b8bc8-113">當您的應用程式在其回呼中收到 **DisconnectedNotification** 類型時，不需要呼叫它。</span><span class="sxs-lookup"><span data-stu-id="b8bc8-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bc8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8bc8-114">Requirements</span></span>



| <span data-ttu-id="b8bc8-115">需求</span><span class="sxs-lookup"><span data-stu-id="b8bc8-115">Requirement</span></span> | <span data-ttu-id="b8bc8-116">值</span><span class="sxs-lookup"><span data-stu-id="b8bc8-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bc8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8bc8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8bc8-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8bc8-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b8bc8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8bc8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8bc8-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8bc8-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8bc8-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b8bc8-121">End of client support</span></span><br/>    | <span data-ttu-id="b8bc8-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b8bc8-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="b8bc8-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b8bc8-123">End of server support</span></span><br/>    | <span data-ttu-id="b8bc8-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8bc8-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="b8bc8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b8bc8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8bc8-126"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8bc8-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="b8bc8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8bc8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8bc8-128"><dt>Wifidisplay .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8bc8-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8bc8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b8bc8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8bc8-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8bc8-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8bc8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8bc8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8bc8-132">**WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="b8bc8-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




