---
description: 定義回呼函式&\# 郵件; 您可以在應用程式中執行此函式，&\# 郵件; 也就是指定給 WFDStartDisplaySink 函式的應用程式。
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: 'WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK 回呼函數 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980832"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="12c10-103">WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼回呼函式</span><span class="sxs-lookup"><span data-stu-id="12c10-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="12c10-104">[ **WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回檔** 函式] 會定義回呼函式（您在應用程式中所執行），此函式是指定給 [**WFDStartDisplaySink**](wfdstartdisplaysink.md) 函式的函數。</span><span class="sxs-lookup"><span data-stu-id="12c10-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c10-105">語法</span><span class="sxs-lookup"><span data-stu-id="12c10-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="12c10-106">參數</span><span class="sxs-lookup"><span data-stu-id="12c10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c10-107">*pvCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="12c10-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12c10-108">傳遞給回呼函式的選擇性內容指標。</span><span class="sxs-lookup"><span data-stu-id="12c10-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="12c10-109">*pNotification* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12c10-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c10-110">結構的指標，其中包含有關顯示接收通知的資料。</span><span class="sxs-lookup"><span data-stu-id="12c10-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="12c10-111">*pNotificationResult* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="12c10-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12c10-112">結構的指標，其中包含您的應用程式可以選擇性地設定的資料，以表示處理顯示接收通知的結果。</span><span class="sxs-lookup"><span data-stu-id="12c10-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12c10-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="12c10-113">Requirements</span></span>



| <span data-ttu-id="12c10-114">需求</span><span class="sxs-lookup"><span data-stu-id="12c10-114">Requirement</span></span> | <span data-ttu-id="12c10-115">值</span><span class="sxs-lookup"><span data-stu-id="12c10-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12c10-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12c10-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12c10-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12c10-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="12c10-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12c10-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12c10-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12c10-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="12c10-120">標頭</span><span class="sxs-lookup"><span data-stu-id="12c10-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c10-121"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="12c10-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




