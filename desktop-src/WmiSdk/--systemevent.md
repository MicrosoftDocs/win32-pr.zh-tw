---
description: 表示系統事件。
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: __SystemEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194151"
---
# <a name="__systemevent-class"></a><span data-ttu-id="83f8c-103">\_\_SystemEvent 類別</span><span class="sxs-lookup"><span data-stu-id="83f8c-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="83f8c-104">**\_ \_ SystemEvent** 系統類別代表系統事件。</span><span class="sxs-lookup"><span data-stu-id="83f8c-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="83f8c-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="83f8c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="83f8c-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="83f8c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f8c-107">語法</span><span class="sxs-lookup"><span data-stu-id="83f8c-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="83f8c-108">成員</span><span class="sxs-lookup"><span data-stu-id="83f8c-108">Members</span></span>

<span data-ttu-id="83f8c-109">**\_ \_ SystemEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83f8c-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="83f8c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="83f8c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83f8c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="83f8c-111">Properties</span></span>

<span data-ttu-id="83f8c-112">**\_ \_ SystemEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="83f8c-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83f8c-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="83f8c-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83f8c-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="83f8c-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="83f8c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83f8c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83f8c-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="83f8c-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="83f8c-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="83f8c-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="83f8c-118">在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)中 (ACL) 的 **Null** 存取控制清單會將無限存取權授與所有人。</span><span class="sxs-lookup"><span data-stu-id="83f8c-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="83f8c-119">如需詳細資訊，請參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="83f8c-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="83f8c-120">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="83f8c-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83f8c-121">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="83f8c-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83f8c-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83f8c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83f8c-123">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="83f8c-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="83f8c-124">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="83f8c-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="83f8c-125">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="83f8c-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="83f8c-126">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="83f8c-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="83f8c-127">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="83f8c-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83f8c-128">備註</span><span class="sxs-lookup"><span data-stu-id="83f8c-128">Remarks</span></span>

<span data-ttu-id="83f8c-129">**\_ \_ SystemEvent** 類別衍生自 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)類別。</span><span class="sxs-lookup"><span data-stu-id="83f8c-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="83f8c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="83f8c-130">Requirements</span></span>



| <span data-ttu-id="83f8c-131">需求</span><span class="sxs-lookup"><span data-stu-id="83f8c-131">Requirement</span></span> | <span data-ttu-id="83f8c-132">值</span><span class="sxs-lookup"><span data-stu-id="83f8c-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="83f8c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83f8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="83f8c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83f8c-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="83f8c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83f8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="83f8c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83f8c-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="83f8c-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="83f8c-137">Namespace</span></span><br/>                | <span data-ttu-id="83f8c-138">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="83f8c-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="83f8c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83f8c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f8c-140">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="83f8c-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="83f8c-141">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="83f8c-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

