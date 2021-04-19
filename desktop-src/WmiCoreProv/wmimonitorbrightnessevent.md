---
description: 代表監視的亮度變更。
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: WmiMonitorBrightnessEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980432"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="f484d-103">WmiMonitorBrightnessEvent 類別</span><span class="sxs-lookup"><span data-stu-id="f484d-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="f484d-104">**WmiMonitorBrightnessEvent** WMI 事件類別代表監視的亮度變更。</span><span class="sxs-lookup"><span data-stu-id="f484d-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f484d-105">語法</span><span class="sxs-lookup"><span data-stu-id="f484d-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="f484d-106">成員</span><span class="sxs-lookup"><span data-stu-id="f484d-106">Members</span></span>

<span data-ttu-id="f484d-107">**WmiMonitorBrightnessEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f484d-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f484d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f484d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f484d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f484d-109">Properties</span></span>

<span data-ttu-id="f484d-110">**WmiMonitorBrightnessEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f484d-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f484d-111">**使用中**</span><span class="sxs-lookup"><span data-stu-id="f484d-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f484d-112">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f484d-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f484d-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f484d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f484d-114">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="f484d-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="f484d-115">**亮度**</span><span class="sxs-lookup"><span data-stu-id="f484d-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f484d-116">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="f484d-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f484d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f484d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f484d-118">目前監視的亮度（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="f484d-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="f484d-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f484d-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f484d-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f484d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f484d-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f484d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f484d-122">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f484d-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f484d-123">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f484d-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f484d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f484d-124">Requirements</span></span>



| <span data-ttu-id="f484d-125">需求</span><span class="sxs-lookup"><span data-stu-id="f484d-125">Requirement</span></span> | <span data-ttu-id="f484d-126">值</span><span class="sxs-lookup"><span data-stu-id="f484d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f484d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f484d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f484d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f484d-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f484d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f484d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f484d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f484d-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f484d-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="f484d-131">Namespace</span></span><br/>                | <span data-ttu-id="f484d-132">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="f484d-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f484d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f484d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f484d-134"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="f484d-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f484d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f484d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f484d-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f484d-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f484d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f484d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f484d-138">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="f484d-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="f484d-139">**WmiMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="f484d-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="f484d-140">接收 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="f484d-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

