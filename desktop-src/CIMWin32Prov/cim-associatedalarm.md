---
description: CIM AssociatedAlarm 相依性會將警示 \_ 與邏輯裝置產生關聯。
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: CIM_AssociatedAlarm 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689031"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="830c1-103">CIM \_ AssociatedAlarm 類別</span><span class="sxs-lookup"><span data-stu-id="830c1-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="830c1-104">**CIM \_ AssociatedAlarm** 相依性會將警示與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="830c1-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="830c1-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="830c1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="830c1-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="830c1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="830c1-107">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="830c1-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="830c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="830c1-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="830c1-109">成員</span><span class="sxs-lookup"><span data-stu-id="830c1-109">Members</span></span>

<span data-ttu-id="830c1-110">**CIM \_ AssociatedAlarm** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="830c1-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="830c1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="830c1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="830c1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="830c1-112">Properties</span></span>

<span data-ttu-id="830c1-113">**CIM \_ AssociatedAlarm** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="830c1-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="830c1-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="830c1-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="830c1-115">資料類型： **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="830c1-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="830c1-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="830c1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="830c1-117">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="830c1-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="830c1-118">包含警報裝置的 [**CIM \_ AlarmDevice**](cim-alarmdevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="830c1-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="830c1-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="830c1-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="830c1-120">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="830c1-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="830c1-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="830c1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="830c1-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="830c1-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="830c1-123">包含發出的邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="830c1-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="830c1-124">備註</span><span class="sxs-lookup"><span data-stu-id="830c1-124">Remarks</span></span>

<span data-ttu-id="830c1-125">**Cim \_ AssociatedAlarm** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="830c1-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="830c1-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="830c1-126">WMI does not implement this class.</span></span>

<span data-ttu-id="830c1-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="830c1-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="830c1-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="830c1-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="830c1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="830c1-129">Requirements</span></span>



| <span data-ttu-id="830c1-130">需求</span><span class="sxs-lookup"><span data-stu-id="830c1-130">Requirement</span></span> | <span data-ttu-id="830c1-131">值</span><span class="sxs-lookup"><span data-stu-id="830c1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="830c1-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="830c1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="830c1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="830c1-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="830c1-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="830c1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="830c1-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="830c1-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="830c1-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="830c1-136">Namespace</span></span><br/>                | <span data-ttu-id="830c1-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="830c1-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="830c1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="830c1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="830c1-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="830c1-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="830c1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="830c1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="830c1-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="830c1-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="830c1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="830c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="830c1-143">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="830c1-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

