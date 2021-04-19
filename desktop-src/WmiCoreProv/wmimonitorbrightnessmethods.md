---
description: 包含管理監視亮度的方法。
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: WmiMonitorBrightnessMethods 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999912"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="e9501-103">WmiMonitorBrightnessMethods 類別</span><span class="sxs-lookup"><span data-stu-id="e9501-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="e9501-104">**WmiMonitorBrightnessMethods** WMI 類別包含管理監視器亮度的方法。</span><span class="sxs-lookup"><span data-stu-id="e9501-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9501-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9501-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="e9501-106">成員</span><span class="sxs-lookup"><span data-stu-id="e9501-106">Members</span></span>

<span data-ttu-id="e9501-107">**WmiMonitorBrightnessMethods** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e9501-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="e9501-108">方法</span><span class="sxs-lookup"><span data-stu-id="e9501-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="e9501-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e9501-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9501-110">方法</span><span class="sxs-lookup"><span data-stu-id="e9501-110">Methods</span></span>

<span data-ttu-id="e9501-111">**WmiMonitorBrightnessMethods** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e9501-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="e9501-112">方法</span><span class="sxs-lookup"><span data-stu-id="e9501-112">Method</span></span>                                                                                                         | <span data-ttu-id="e9501-113">描述</span><span class="sxs-lookup"><span data-stu-id="e9501-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="e9501-114">**WmiRevertToPolicyBrightness**</span><span class="sxs-lookup"><span data-stu-id="e9501-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="e9501-115">將亮度設定回原則設定。</span><span class="sxs-lookup"><span data-stu-id="e9501-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="e9501-116">**WmiSetALSBrightness**</span><span class="sxs-lookup"><span data-stu-id="e9501-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="e9501-117">設定環境光源感應器的亮度值。</span><span class="sxs-lookup"><span data-stu-id="e9501-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="e9501-118">**WmiSetALSBrightnessState**</span><span class="sxs-lookup"><span data-stu-id="e9501-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="e9501-119">控制環境光線感應器的亮度狀態。</span><span class="sxs-lookup"><span data-stu-id="e9501-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="e9501-120">**WmiSetBrightness**</span><span class="sxs-lookup"><span data-stu-id="e9501-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="e9501-121">設定監視亮度。</span><span class="sxs-lookup"><span data-stu-id="e9501-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="e9501-122">屬性</span><span class="sxs-lookup"><span data-stu-id="e9501-122">Properties</span></span>

<span data-ttu-id="e9501-123">**WmiMonitorBrightnessMethods** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e9501-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9501-124">**使用中**</span><span class="sxs-lookup"><span data-stu-id="e9501-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9501-125">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e9501-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9501-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e9501-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9501-127">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="e9501-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e9501-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="e9501-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9501-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e9501-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9501-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e9501-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9501-131">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="e9501-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e9501-132">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9501-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9501-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9501-133">Requirements</span></span>



| <span data-ttu-id="e9501-134">需求</span><span class="sxs-lookup"><span data-stu-id="e9501-134">Requirement</span></span> | <span data-ttu-id="e9501-135">值</span><span class="sxs-lookup"><span data-stu-id="e9501-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9501-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9501-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e9501-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9501-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e9501-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9501-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e9501-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9501-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e9501-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9501-140">Namespace</span></span><br/>                | <span data-ttu-id="e9501-141">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="e9501-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e9501-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e9501-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9501-143"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9501-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9501-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e9501-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9501-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9501-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9501-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9501-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9501-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="e9501-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




