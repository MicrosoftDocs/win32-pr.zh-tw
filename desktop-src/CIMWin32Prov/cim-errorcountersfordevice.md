---
description: CIM \_ ErrorCountersForDevice 類別會將 cim \_ DeviceErrorCounts 類別與它所套用的邏輯裝置產生關聯。
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: CIM_ErrorCountersForDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847364"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="7a075-103">CIM \_ ErrorCountersForDevice 類別</span><span class="sxs-lookup"><span data-stu-id="7a075-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="7a075-104">**Cim \_ ErrorCountersForDevice** 類別會將 [**cim \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)類別與它所套用的邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="7a075-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a075-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7a075-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7a075-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7a075-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7a075-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a075-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7a075-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7a075-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a075-109">語法</span><span class="sxs-lookup"><span data-stu-id="7a075-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="7a075-110">成員</span><span class="sxs-lookup"><span data-stu-id="7a075-110">Members</span></span>

<span data-ttu-id="7a075-111">**CIM \_ ErrorCountersForDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7a075-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="7a075-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7a075-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a075-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7a075-113">Properties</span></span>

<span data-ttu-id="7a075-114">**CIM \_ ErrorCountersForDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7a075-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a075-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a075-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a075-116">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="7a075-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="7a075-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a075-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a075-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Element" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="7a075-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7a075-119">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述錯誤計數器適用的裝置。</span><span class="sxs-lookup"><span data-stu-id="7a075-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="7a075-120">**統計**</span><span class="sxs-lookup"><span data-stu-id="7a075-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a075-121">資料類型： **CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="7a075-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="7a075-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7a075-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a075-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Stats" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="7a075-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7a075-124">描述統計物件的 [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) -在此案例中為錯誤計數器類別。</span><span class="sxs-lookup"><span data-stu-id="7a075-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a075-125">備註</span><span class="sxs-lookup"><span data-stu-id="7a075-125">Remarks</span></span>

<span data-ttu-id="7a075-126">**Cim \_ ErrorCountersForDevice** 類別繼承自 [**cim \_ 統計資料**](cim-statistics.md)。</span><span class="sxs-lookup"><span data-stu-id="7a075-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="7a075-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="7a075-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7a075-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7a075-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7a075-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7a075-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a075-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a075-130">Requirements</span></span>



| <span data-ttu-id="7a075-131">需求</span><span class="sxs-lookup"><span data-stu-id="7a075-131">Requirement</span></span> | <span data-ttu-id="7a075-132">值</span><span class="sxs-lookup"><span data-stu-id="7a075-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a075-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7a075-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a075-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a075-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a075-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7a075-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a075-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a075-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="7a075-137">Namespace</span></span><br/>                | <span data-ttu-id="7a075-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a075-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a075-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7a075-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a075-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a075-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a075-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7a075-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a075-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a075-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a075-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a075-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a075-144">**CIM \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="7a075-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 

