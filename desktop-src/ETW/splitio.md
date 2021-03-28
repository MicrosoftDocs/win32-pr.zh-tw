---
description: 這個類別是分割 IO 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: SplitIo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972793"
---
# <a name="splitio-class"></a><span data-ttu-id="2730c-104">SplitIo 類別</span><span class="sxs-lookup"><span data-stu-id="2730c-104">SplitIo class</span></span>

<span data-ttu-id="2730c-105">這個類別是分割 IO 事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="2730c-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="2730c-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="2730c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2730c-107">語法</span><span class="sxs-lookup"><span data-stu-id="2730c-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="2730c-108">成員</span><span class="sxs-lookup"><span data-stu-id="2730c-108">Members</span></span>

<span data-ttu-id="2730c-109">**SplitIo** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="2730c-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="2730c-110">備註</span><span class="sxs-lookup"><span data-stu-id="2730c-110">Remarks</span></span>

<span data-ttu-id="2730c-111">若要在 NT 核心記錄會話中啟用分割 IO 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 分割 \_ io** 旗標。</span><span class="sxs-lookup"><span data-stu-id="2730c-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="2730c-112">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**SplitIoGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對分割 IO 事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="2730c-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="2730c-113">使用下列事件種類來識別使用事件時的實際事件。</span><span class="sxs-lookup"><span data-stu-id="2730c-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="2730c-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="2730c-114">Event type</span></span>           | <span data-ttu-id="2730c-115">描述</span><span class="sxs-lookup"><span data-stu-id="2730c-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2730c-116">事件種類值，32</span><span class="sxs-lookup"><span data-stu-id="2730c-116">Event type value, 32</span></span> | <span data-ttu-id="2730c-117">分割 IO 事件。</span><span class="sxs-lookup"><span data-stu-id="2730c-117">Split IO event.</span></span> <span data-ttu-id="2730c-118">[**SplitIo \_ 資訊**](splitio-info.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="2730c-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="2730c-119">分割 IO 事件表示因為基礎鏡像磁片硬體，IO 要求已分割成多個磁片 IO 要求。</span><span class="sxs-lookup"><span data-stu-id="2730c-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="2730c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2730c-120">Requirements</span></span>



| <span data-ttu-id="2730c-121">需求</span><span class="sxs-lookup"><span data-stu-id="2730c-121">Requirement</span></span> | <span data-ttu-id="2730c-122">值</span><span class="sxs-lookup"><span data-stu-id="2730c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2730c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2730c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2730c-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2730c-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2730c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2730c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2730c-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2730c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
