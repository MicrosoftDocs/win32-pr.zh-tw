---
description: '>register-wmievent 類別是衍生所有 WMI 事件類別的基類。'
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: '>register-wmievent 類別'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027314"
---
# <a name="wmievent-class"></a><span data-ttu-id="6bac1-103">>register-wmievent 類別</span><span class="sxs-lookup"><span data-stu-id="6bac1-103">WMIEvent class</span></span>

<span data-ttu-id="6bac1-104">**>register-wmievent** 類別是衍生所有 WMI 事件類別的基類。</span><span class="sxs-lookup"><span data-stu-id="6bac1-104">The **WMIEvent** class is a base class from which all WMI event classes are derived.</span></span>

<span data-ttu-id="6bac1-105">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bac1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6bac1-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="6bac1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bac1-107">語法</span><span class="sxs-lookup"><span data-stu-id="6bac1-107">Syntax</span></span>

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="6bac1-108">成員</span><span class="sxs-lookup"><span data-stu-id="6bac1-108">Members</span></span>

<span data-ttu-id="6bac1-109">**>register-wmievent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6bac1-109">The **WMIEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6bac1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6bac1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6bac1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6bac1-111">Properties</span></span>

<span data-ttu-id="6bac1-112">**>register-wmievent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6bac1-112">The **WMIEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6bac1-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="6bac1-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bac1-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="6bac1-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6bac1-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bac1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bac1-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="6bac1-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="6bac1-117">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="6bac1-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="6bac1-118">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。</span><span class="sxs-lookup"><span data-stu-id="6bac1-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="6bac1-119">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="6bac1-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bac1-120">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6bac1-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6bac1-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bac1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bac1-122">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="6bac1-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="6bac1-123">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="6bac1-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="6bac1-124">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="6bac1-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="6bac1-125">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="6bac1-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="6bac1-126">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6bac1-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bac1-127">備註</span><span class="sxs-lookup"><span data-stu-id="6bac1-127">Remarks</span></span>

<span data-ttu-id="6bac1-128">**>register-wmievent** 類別衍生自 [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)。</span><span class="sxs-lookup"><span data-stu-id="6bac1-128">The **WMIEvent** class is derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bac1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bac1-129">Requirements</span></span>



| <span data-ttu-id="6bac1-130">需求</span><span class="sxs-lookup"><span data-stu-id="6bac1-130">Requirement</span></span> | <span data-ttu-id="6bac1-131">值</span><span class="sxs-lookup"><span data-stu-id="6bac1-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bac1-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bac1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6bac1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bac1-133">Windows Vista</span></span><br/>                                                                                                                              |
| <span data-ttu-id="6bac1-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bac1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6bac1-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6bac1-135">Windows Server 2003</span></span><br/>                                                                                                                        |
| <span data-ttu-id="6bac1-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="6bac1-136">Namespace</span></span><br/>                | <span data-ttu-id="6bac1-137">根 \\ WMI</span><span class="sxs-lookup"><span data-stu-id="6bac1-137">Root\\WMI</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="6bac1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6bac1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bac1-139"><dt>Wmi. mof;</dt><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bac1-139"><dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bac1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6bac1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bac1-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bac1-141"><dt>WmiProv.dll</dt></span></span> </dl>                                                                |



## <a name="see-also"></a><span data-ttu-id="6bac1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bac1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bac1-143">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="6bac1-143">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="6bac1-144">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="6bac1-144">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

