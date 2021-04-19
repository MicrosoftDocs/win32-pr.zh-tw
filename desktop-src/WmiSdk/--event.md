---
description: 是抽象基類，作為所有內建和外建事件的父類別。
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: __Event 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997997"
---
# <a name="__event-class"></a><span data-ttu-id="9cd41-103">\_\_事件類別</span><span class="sxs-lookup"><span data-stu-id="9cd41-103">\_\_Event class</span></span>

<span data-ttu-id="9cd41-104">**\_ \_ 事件** 系統類別是一個抽象基類，做為所有內建和外來事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="9cd41-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="9cd41-105">所有新的事件種類最終都必須衍生自 **\_ \_ 事件**。</span><span class="sxs-lookup"><span data-stu-id="9cd41-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="9cd41-106">內部事件直接衍生自這個類別。</span><span class="sxs-lookup"><span data-stu-id="9cd41-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="9cd41-107">使用者定義的外建事件是衍生自這個類別的子類別，稱為 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)。</span><span class="sxs-lookup"><span data-stu-id="9cd41-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="9cd41-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9cd41-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9cd41-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9cd41-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd41-110">語法</span><span class="sxs-lookup"><span data-stu-id="9cd41-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="9cd41-111">成員</span><span class="sxs-lookup"><span data-stu-id="9cd41-111">Members</span></span>

<span data-ttu-id="9cd41-112">**\_ \_ 事件** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9cd41-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="9cd41-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9cd41-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9cd41-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9cd41-114">Properties</span></span>

<span data-ttu-id="9cd41-115">**\_ \_ 事件** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9cd41-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9cd41-116">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="9cd41-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cd41-117">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cd41-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9cd41-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cd41-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cd41-119">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="9cd41-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="9cd41-120">如需詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9cd41-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9cd41-121">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="9cd41-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cd41-122">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cd41-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cd41-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cd41-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cd41-124">指出事件產生時間的唯一值。</span><span class="sxs-lookup"><span data-stu-id="9cd41-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="9cd41-125">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="9cd41-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="9cd41-126">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="9cd41-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="9cd41-127">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="9cd41-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cd41-128">備註</span><span class="sxs-lookup"><span data-stu-id="9cd41-128">Remarks</span></span>

<span data-ttu-id="9cd41-129">**\_ \_ 事件** 類別衍生自沒有屬性的 [**\_ \_ IndicationRelated**](--indicationrelated.md)。</span><span class="sxs-lookup"><span data-stu-id="9cd41-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd41-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cd41-130">Requirements</span></span>



| <span data-ttu-id="9cd41-131">需求</span><span class="sxs-lookup"><span data-stu-id="9cd41-131">Requirement</span></span> | <span data-ttu-id="9cd41-132">值</span><span class="sxs-lookup"><span data-stu-id="9cd41-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9cd41-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9cd41-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd41-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cd41-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9cd41-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9cd41-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd41-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cd41-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="9cd41-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="9cd41-137">Namespace</span></span><br/>                | <span data-ttu-id="9cd41-138">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="9cd41-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="9cd41-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cd41-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd41-140">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="9cd41-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="9cd41-141">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="9cd41-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="9cd41-142">判斷要接收的事件種類</span><span class="sxs-lookup"><span data-stu-id="9cd41-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="9cd41-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="9cd41-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="9cd41-144">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="9cd41-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="9cd41-145">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="9cd41-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

