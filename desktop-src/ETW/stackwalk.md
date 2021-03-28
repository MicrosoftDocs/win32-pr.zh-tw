---
description: 這個類別是堆疊追蹤事件的父類別。
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: StackWalk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972184"
---
# <a name="stackwalk-class"></a><span data-ttu-id="f3b2e-103">StackWalk 類別</span><span class="sxs-lookup"><span data-stu-id="f3b2e-103">StackWalk class</span></span>

<span data-ttu-id="f3b2e-104">這個類別是堆疊追蹤事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="f3b2e-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b2e-106">語法</span><span class="sxs-lookup"><span data-stu-id="f3b2e-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f3b2e-107">成員</span><span class="sxs-lookup"><span data-stu-id="f3b2e-107">Members</span></span>

<span data-ttu-id="f3b2e-108">**StackWalk** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b2e-109">備註</span><span class="sxs-lookup"><span data-stu-id="f3b2e-109">Remarks</span></span>

<span data-ttu-id="f3b2e-110">若要啟用核心事件的堆疊追蹤，請呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函式，並指定您想要用來捕捉堆疊追蹤的核心事件和類型。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="f3b2e-111">若要啟用其他事件的堆疊追蹤，請將 [[**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)的 **EnableProperty** 成員] 設定為 [**事件 \_ 啟用 \_ 屬性 \_ 堆疊 \_ 追蹤**]。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="f3b2e-112">使用下列事件種類來識別使用事件時的實際事件。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="f3b2e-113">事件類型</span><span class="sxs-lookup"><span data-stu-id="f3b2e-113">Event type</span></span>           | <span data-ttu-id="f3b2e-114">描述</span><span class="sxs-lookup"><span data-stu-id="f3b2e-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b2e-115">事件種類值，32</span><span class="sxs-lookup"><span data-stu-id="f3b2e-115">Event type value, 32</span></span> | <span data-ttu-id="f3b2e-116">堆疊追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-116">Stack tracing event.</span></span> <span data-ttu-id="f3b2e-117">[**StackWalk \_ 事件**](stackwalk-event.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="f3b2e-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f3b2e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3b2e-118">Requirements</span></span>



| <span data-ttu-id="f3b2e-119">需求</span><span class="sxs-lookup"><span data-stu-id="f3b2e-119">Requirement</span></span> | <span data-ttu-id="f3b2e-120">值</span><span class="sxs-lookup"><span data-stu-id="f3b2e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f3b2e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3b2e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b2e-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3b2e-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f3b2e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3b2e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b2e-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3b2e-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
