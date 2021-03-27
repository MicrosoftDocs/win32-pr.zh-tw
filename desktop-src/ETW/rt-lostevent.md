---
description: 此事件種類類別用來指出在即時會話中遺失事件。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511584"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="d3826-104">RT \_ LostEvent 類別</span><span class="sxs-lookup"><span data-stu-id="d3826-104">RT\_LostEvent class</span></span>

<span data-ttu-id="d3826-105">此事件種類類別用來指出在即時會話中遺失事件。</span><span class="sxs-lookup"><span data-stu-id="d3826-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="d3826-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d3826-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3826-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3826-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="d3826-108">成員</span><span class="sxs-lookup"><span data-stu-id="d3826-108">Members</span></span>

<span data-ttu-id="d3826-109">**RT \_ LostEvent** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="d3826-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3826-110">備註</span><span class="sxs-lookup"><span data-stu-id="d3826-110">Remarks</span></span>

<span data-ttu-id="d3826-111">RTLostEvent 事件種類指出有一或多個事件遺失。</span><span class="sxs-lookup"><span data-stu-id="d3826-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="d3826-112">RTLostBuffer 事件種類指出有一或多個緩衝區遺失。</span><span class="sxs-lookup"><span data-stu-id="d3826-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="d3826-113">RTLostEvent 和 RTLostBuffer 事件種類會在處理緩衝區中的事件之前傳遞。</span><span class="sxs-lookup"><span data-stu-id="d3826-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="d3826-114">RTLostFile 表示自動記錄器用來捕捉事件的支援檔案已遺失。</span><span class="sxs-lookup"><span data-stu-id="d3826-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="d3826-115">遺失事件取決於記錄事件的頻率，以及取用者花費多少時間來處理事件。</span><span class="sxs-lookup"><span data-stu-id="d3826-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3826-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3826-116">Requirements</span></span>



| <span data-ttu-id="d3826-117">需求</span><span class="sxs-lookup"><span data-stu-id="d3826-117">Requirement</span></span> | <span data-ttu-id="d3826-118">值</span><span class="sxs-lookup"><span data-stu-id="d3826-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="d3826-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3826-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3826-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3826-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d3826-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3826-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3826-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="d3826-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="d3826-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3826-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3826-124">**遺失的 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="d3826-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




