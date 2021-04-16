---
description: 指定如何為取用者產生計時器事件的指示。
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321015"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="63631-103">\_\_TimerInstruction 類別</span><span class="sxs-lookup"><span data-stu-id="63631-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="63631-104">**\_ \_ TimerInstruction** abstract system 類別指定如何為取用者產生 [計時器事件](receiving-a-timed-or-repeating-event.md)的指示。</span><span class="sxs-lookup"><span data-stu-id="63631-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="63631-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="63631-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="63631-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="63631-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63631-107">語法</span><span class="sxs-lookup"><span data-stu-id="63631-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="63631-108">成員</span><span class="sxs-lookup"><span data-stu-id="63631-108">Members</span></span>

<span data-ttu-id="63631-109">**\_ \_ TimerInstruction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="63631-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="63631-110">屬性</span><span class="sxs-lookup"><span data-stu-id="63631-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63631-111">屬性</span><span class="sxs-lookup"><span data-stu-id="63631-111">Properties</span></span>

<span data-ttu-id="63631-112">**\_ \_ TimerInstruction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="63631-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63631-113">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="63631-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63631-114">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="63631-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63631-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="63631-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63631-116">描述當取用者可供使用時，是否會產生和接收通知事件。</span><span class="sxs-lookup"><span data-stu-id="63631-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="63631-117">FALSE</span><span class="sxs-lookup"><span data-stu-id="63631-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="63631-118">當 WMI 或取用者再次變成可用時，將會產生並接收通知事件。</span><span class="sxs-lookup"><span data-stu-id="63631-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="63631-119">true</span><span class="sxs-lookup"><span data-stu-id="63631-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="63631-120">如果 WMI 無法在適當的時間間隔內產生，或要求接收事件的取用者無法使用，就不會發生計時器事件。</span><span class="sxs-lookup"><span data-stu-id="63631-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63631-121">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="63631-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63631-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="63631-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63631-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="63631-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63631-124">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="63631-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="63631-125">識別此特定計時器事件的唯一使用者指派字串。</span><span class="sxs-lookup"><span data-stu-id="63631-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="63631-126">為了避免與其他計時器識別碼發生名稱衝突，可以使用分散式運算機環境的字串形式 (DCE) 樣式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="63631-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="63631-127">這個屬性是代表事件的 [**\_ \_ TimerEvent**](--timerevent.md)實例的一部分。</span><span class="sxs-lookup"><span data-stu-id="63631-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63631-128">備註</span><span class="sxs-lookup"><span data-stu-id="63631-128">Remarks</span></span>

<span data-ttu-id="63631-129">**\_ \_ TimerInstruction** 類別衍生自 [**\_ \_ EventGenerator**](--eventgenerator.md)。</span><span class="sxs-lookup"><span data-stu-id="63631-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="63631-130">**\_ \_ TimerInstruction** 子類別會 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)，供取用者用來註冊絕對計時器事件，以及用來註冊間隔計時器事件的 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="63631-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="63631-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="63631-131">Requirements</span></span>



| <span data-ttu-id="63631-132">需求</span><span class="sxs-lookup"><span data-stu-id="63631-132">Requirement</span></span> | <span data-ttu-id="63631-133">值</span><span class="sxs-lookup"><span data-stu-id="63631-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="63631-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63631-134">Minimum supported client</span></span><br/> | <span data-ttu-id="63631-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63631-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="63631-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63631-136">Minimum supported server</span></span><br/> | <span data-ttu-id="63631-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63631-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="63631-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="63631-138">Namespace</span></span><br/>                | <span data-ttu-id="63631-139">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="63631-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="63631-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63631-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63631-141">**\_\_EventGenerator**</span><span class="sxs-lookup"><span data-stu-id="63631-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="63631-142">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="63631-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

