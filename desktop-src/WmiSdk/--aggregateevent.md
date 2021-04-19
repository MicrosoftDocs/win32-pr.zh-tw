---
description: 代表數個個別內建或外來事件的匯總事件。
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975274"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="5d539-103">\_\_AggregateEvent 類別</span><span class="sxs-lookup"><span data-stu-id="5d539-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="5d539-104">**\_ \_ AggregateEvent** 系統類別代表數個個別內建或外來事件的匯總事件。</span><span class="sxs-lookup"><span data-stu-id="5d539-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="5d539-105">當取用者向其事件查詢中的 [group](group-clause.md) in 子句註冊時，WMI 會產生 **\_ \_ AggregateEvent** 的實例，而不是 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="5d539-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="5d539-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5d539-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5d539-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5d539-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d539-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d539-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="5d539-109">成員</span><span class="sxs-lookup"><span data-stu-id="5d539-109">Members</span></span>

<span data-ttu-id="5d539-110">**\_ \_ AggregateEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5d539-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5d539-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5d539-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d539-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5d539-112">Properties</span></span>

<span data-ttu-id="5d539-113">**\_ \_ AggregateEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5d539-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d539-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="5d539-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d539-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d539-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d539-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d539-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d539-117">合併以產生這個單一摘要事件的事件數目。</span><span class="sxs-lookup"><span data-stu-id="5d539-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="5d539-118">**Representative**</span><span class="sxs-lookup"><span data-stu-id="5d539-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d539-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="5d539-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5d539-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d539-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d539-121">匯總間隔內傳遞的其中一個事件的複本。</span><span class="sxs-lookup"><span data-stu-id="5d539-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="5d539-122">例如，如果取用者已從登錄事件提供者註冊登錄機碼變更事件， **代表** 會保留 **RegistryKeyChangeEvent** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5d539-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d539-123">備註</span><span class="sxs-lookup"><span data-stu-id="5d539-123">Remarks</span></span>

<span data-ttu-id="5d539-124">**\_ \_ AggregateEvent** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="5d539-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="5d539-125">事件提供者永遠不會產生匯總事件。</span><span class="sxs-lookup"><span data-stu-id="5d539-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="5d539-126">它們必須在處理事件查詢時，忽略子句內的群組。</span><span class="sxs-lookup"><span data-stu-id="5d539-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d539-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d539-127">Requirements</span></span>



| <span data-ttu-id="5d539-128">需求</span><span class="sxs-lookup"><span data-stu-id="5d539-128">Requirement</span></span> | <span data-ttu-id="5d539-129">值</span><span class="sxs-lookup"><span data-stu-id="5d539-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5d539-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d539-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5d539-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d539-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5d539-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d539-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5d539-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d539-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5d539-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="5d539-134">Namespace</span></span><br/>                | <span data-ttu-id="5d539-135">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="5d539-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5d539-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d539-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d539-137">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="5d539-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="5d539-138">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="5d539-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5d539-139">使用 WQL 查詢</span><span class="sxs-lookup"><span data-stu-id="5d539-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

