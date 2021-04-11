---
description: 作為所有使用者定義事件種類（也稱為外建事件）的父類別。
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: __ExtrinsicEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194720"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="83c5e-103">\_\_ExtrinsicEvent 類別</span><span class="sxs-lookup"><span data-stu-id="83c5e-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="83c5e-104">**\_ \_ ExtrinsicEvent** 系統類別是一個抽象基類，做為所有使用者定義事件種類（也稱為外建 [事件](determining-the-type-of-event-to-receive.md)）的父類別。</span><span class="sxs-lookup"><span data-stu-id="83c5e-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="83c5e-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="83c5e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="83c5e-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="83c5e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c5e-107">語法</span><span class="sxs-lookup"><span data-stu-id="83c5e-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="83c5e-108">成員</span><span class="sxs-lookup"><span data-stu-id="83c5e-108">Members</span></span>

<span data-ttu-id="83c5e-109">**\_ \_ ExtrinsicEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83c5e-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="83c5e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="83c5e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83c5e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="83c5e-111">Properties</span></span>

<span data-ttu-id="83c5e-112">**\_ \_ ExtrinsicEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="83c5e-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83c5e-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="83c5e-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c5e-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="83c5e-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="83c5e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83c5e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c5e-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="83c5e-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="83c5e-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="83c5e-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="83c5e-118">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="83c5e-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="83c5e-119">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="83c5e-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c5e-120">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="83c5e-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83c5e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83c5e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c5e-122">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="83c5e-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="83c5e-123">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="83c5e-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="83c5e-124">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="83c5e-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="83c5e-125">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="83c5e-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="83c5e-126">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="83c5e-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83c5e-127">備註</span><span class="sxs-lookup"><span data-stu-id="83c5e-127">Remarks</span></span>

<span data-ttu-id="83c5e-128">**\_ \_ ExtrinsicEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="83c5e-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83c5e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="83c5e-129">Requirements</span></span>



| <span data-ttu-id="83c5e-130">需求</span><span class="sxs-lookup"><span data-stu-id="83c5e-130">Requirement</span></span> | <span data-ttu-id="83c5e-131">值</span><span class="sxs-lookup"><span data-stu-id="83c5e-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="83c5e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83c5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="83c5e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83c5e-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="83c5e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83c5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="83c5e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83c5e-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="83c5e-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="83c5e-136">Namespace</span></span><br/>                | <span data-ttu-id="83c5e-137">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="83c5e-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="83c5e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83c5e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c5e-139">**\_\_事件**</span><span class="sxs-lookup"><span data-stu-id="83c5e-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="83c5e-140">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="83c5e-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

