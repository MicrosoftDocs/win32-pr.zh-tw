---
description: CIM \_ AssociatedSensor 類別會將已安裝的感應器與邏輯裝置產生關聯。 感應器會測量重要的輸入和輸出屬性，並可包含在裝置內或安裝在附近。
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: CIM_AssociatedSensor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847442"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="dc9c2-104">CIM \_ AssociatedSensor 類別</span><span class="sxs-lookup"><span data-stu-id="dc9c2-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="dc9c2-105">**CIM \_ AssociatedSensor** 類別會將已安裝的感應器與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="dc9c2-106">感應器會測量重要的輸入和輸出屬性，並可包含在裝置內或安裝在附近。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc9c2-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dc9c2-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dc9c2-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dc9c2-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9c2-111">語法</span><span class="sxs-lookup"><span data-stu-id="dc9c2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="dc9c2-112">成員</span><span class="sxs-lookup"><span data-stu-id="dc9c2-112">Members</span></span>

<span data-ttu-id="dc9c2-113">**CIM \_ AssociatedSensor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dc9c2-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="dc9c2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="dc9c2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc9c2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="dc9c2-115">Properties</span></span>

<span data-ttu-id="dc9c2-116">**CIM \_ AssociatedSensor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc9c2-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="dc9c2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9c2-118">資料類型： **CIM \_ 感應器**</span><span class="sxs-lookup"><span data-stu-id="dc9c2-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="dc9c2-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc9c2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9c2-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="dc9c2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dc9c2-121">描述感應器的 [**CIM \_ 感應器**](cim-sensor.md) 。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="dc9c2-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="dc9c2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9c2-123">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="dc9c2-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="dc9c2-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc9c2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc9c2-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="dc9c2-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="dc9c2-126">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述由感應器測量其資訊的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc9c2-127">備註</span><span class="sxs-lookup"><span data-stu-id="dc9c2-127">Remarks</span></span>

<span data-ttu-id="dc9c2-128">**Cim \_ AssociatedSensor** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="dc9c2-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-129">WMI does not implement this class.</span></span> <span data-ttu-id="dc9c2-130">如需衍生自 **CIM \_ AssociatedSensor** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dc9c2-131">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dc9c2-132">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dc9c2-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc9c2-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc9c2-133">Requirements</span></span>



| <span data-ttu-id="dc9c2-134">需求</span><span class="sxs-lookup"><span data-stu-id="dc9c2-134">Requirement</span></span> | <span data-ttu-id="dc9c2-135">值</span><span class="sxs-lookup"><span data-stu-id="dc9c2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9c2-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc9c2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9c2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc9c2-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc9c2-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc9c2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9c2-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc9c2-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc9c2-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc9c2-140">Namespace</span></span><br/>                | <span data-ttu-id="dc9c2-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dc9c2-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc9c2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="dc9c2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc9c2-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc9c2-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc9c2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dc9c2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc9c2-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc9c2-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9c2-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc9c2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9c2-147">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="dc9c2-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

