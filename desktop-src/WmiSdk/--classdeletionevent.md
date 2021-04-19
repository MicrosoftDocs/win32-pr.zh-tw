---
description: 表示類別刪除事件，這是從命名空間移除類別時所產生的內建事件種類。
ms.assetid: dd44c03e-4d0d-4750-942d-495893d21650
ms.tgt_platform: multiple
title: __ClassDeletionEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29242335edeffbdc44deebb3acacd5631fcc7b68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977957"
---
# <a name="__classdeletionevent-class"></a><span data-ttu-id="ce6a3-103">\_\_ClassDeletionEvent 類別</span><span class="sxs-lookup"><span data-stu-id="ce6a3-103">\_\_ClassDeletionEvent class</span></span>

<span data-ttu-id="ce6a3-104">**\_ \_ ClassDeletionEvent** 系統類別代表類別刪除事件，這是從命名空間移除類別時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-104">The **\_\_ClassDeletionEvent** system class represents a class deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is removed from the namespace.</span></span>

<span data-ttu-id="ce6a3-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ce6a3-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce6a3-107">Syntax</span></span>

``` syntax
class __ClassDeletionEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ce6a3-108">成員</span><span class="sxs-lookup"><span data-stu-id="ce6a3-108">Members</span></span>

<span data-ttu-id="ce6a3-109">**\_ \_ ClassDeletionEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ce6a3-109">The **\_\_ClassDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ce6a3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ce6a3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce6a3-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ce6a3-111">Properties</span></span>

<span data-ttu-id="ce6a3-112">**\_ \_ ClassDeletionEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-112">The **\_\_ClassDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce6a3-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="ce6a3-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6a3-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="ce6a3-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ce6a3-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce6a3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce6a3-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ce6a3-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce6a3-118">**>targetclass**</span><span class="sxs-lookup"><span data-stu-id="ce6a3-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6a3-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ce6a3-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ce6a3-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce6a3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce6a3-121">類別刪除事件所報告之新刪除類別的複本。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-121">Copy of the newly deleted class reported by the class deletion event.</span></span> <span data-ttu-id="ce6a3-122">這個屬性繼承自 [**\_ \_ ClassOperationEvent**](--classoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce6a3-123">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="ce6a3-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6a3-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ce6a3-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ce6a3-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce6a3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce6a3-126">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ce6a3-127">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ce6a3-128">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-128">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="ce6a3-129">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ce6a3-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce6a3-131">備註</span><span class="sxs-lookup"><span data-stu-id="ce6a3-131">Remarks</span></span>

<span data-ttu-id="ce6a3-132">**\_ \_ ClassDeletionEvent** 類別衍生自 [**\_ \_ ClassOperationEvent**](--classoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="ce6a3-132">The **\_\_ClassDeletionEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6a3-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce6a3-133">Requirements</span></span>



| <span data-ttu-id="ce6a3-134">需求</span><span class="sxs-lookup"><span data-stu-id="ce6a3-134">Requirement</span></span> | <span data-ttu-id="ce6a3-135">值</span><span class="sxs-lookup"><span data-stu-id="ce6a3-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ce6a3-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce6a3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6a3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce6a3-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ce6a3-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce6a3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6a3-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce6a3-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ce6a3-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="ce6a3-140">Namespace</span></span><br/>                | <span data-ttu-id="ce6a3-141">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="ce6a3-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ce6a3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce6a3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6a3-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="ce6a3-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="ce6a3-144">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="ce6a3-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

