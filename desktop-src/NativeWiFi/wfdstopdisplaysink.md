---
description: 停止 Miracast 接收模式、關閉可探索性，並取消註冊回呼。
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: 'WFDDisplaySinkStop 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974991"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="f924a-103">WFDDisplaySinkStop 函式</span><span class="sxs-lookup"><span data-stu-id="f924a-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="f924a-104">停止 Miracast 接收模式、關閉可探索性，並取消註冊回呼。</span><span class="sxs-lookup"><span data-stu-id="f924a-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="f924a-105">您的應用程式應該在關機時呼叫此一次。</span><span class="sxs-lookup"><span data-stu-id="f924a-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="f924a-106">語法</span><span class="sxs-lookup"><span data-stu-id="f924a-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="f924a-107">參數</span><span class="sxs-lookup"><span data-stu-id="f924a-107">Parameters</span></span>

<span data-ttu-id="f924a-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f924a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f924a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f924a-109">Return value</span></span>

<span data-ttu-id="f924a-110">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="f924a-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="f924a-111">備註</span><span class="sxs-lookup"><span data-stu-id="f924a-111">Remarks</span></span>

<span data-ttu-id="f924a-112">在呼叫 **WFDStopDisplaySink** 之前，您的應用程式應該已解除封鎖任何進行中的回呼。</span><span class="sxs-lookup"><span data-stu-id="f924a-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f924a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f924a-113">Requirements</span></span>



| <span data-ttu-id="f924a-114">需求</span><span class="sxs-lookup"><span data-stu-id="f924a-114">Requirement</span></span> | <span data-ttu-id="f924a-115">值</span><span class="sxs-lookup"><span data-stu-id="f924a-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f924a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f924a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f924a-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f924a-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f924a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f924a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f924a-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f924a-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f924a-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f924a-120">End of client support</span></span><br/>    | <span data-ttu-id="f924a-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f924a-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="f924a-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f924a-122">End of server support</span></span><br/>    | <span data-ttu-id="f924a-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f924a-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="f924a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f924a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f924a-125"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="f924a-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="f924a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="f924a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f924a-127"><dt>Wifidisplay .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f924a-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="f924a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f924a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f924a-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f924a-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




