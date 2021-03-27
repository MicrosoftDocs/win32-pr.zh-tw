---
description: 記錄標頭事件的父類別。 此類別一律是第一個傳送至取用者的事件追蹤類別 (此事件不會傳送給即時取用者) 。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: EventTraceEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972208"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="5a0ef-105">EventTraceEvent 類別</span><span class="sxs-lookup"><span data-stu-id="5a0ef-105">EventTraceEvent class</span></span>

<span data-ttu-id="5a0ef-106">記錄標頭事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="5a0ef-106">The parent class for log header events.</span></span> <span data-ttu-id="5a0ef-107">此類別一律是第一個傳送至取用者的事件追蹤類別 (此事件不會傳送給即時取用者) 。</span><span class="sxs-lookup"><span data-stu-id="5a0ef-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="5a0ef-108">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="5a0ef-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0ef-109">語法</span><span class="sxs-lookup"><span data-stu-id="5a0ef-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="5a0ef-110">成員</span><span class="sxs-lookup"><span data-stu-id="5a0ef-110">Members</span></span>

<span data-ttu-id="5a0ef-111">**EventTraceEvent** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="5a0ef-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0ef-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a0ef-112">Requirements</span></span>



| <span data-ttu-id="5a0ef-113">需求</span><span class="sxs-lookup"><span data-stu-id="5a0ef-113">Requirement</span></span> | <span data-ttu-id="5a0ef-114">值</span><span class="sxs-lookup"><span data-stu-id="5a0ef-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a0ef-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a0ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0ef-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a0ef-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5a0ef-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a0ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0ef-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a0ef-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a0ef-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a0ef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0ef-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="5a0ef-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="5a0ef-121">**EventTrace \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="5a0ef-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




