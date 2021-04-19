---
description: 代表 (SAP) 的服務存取點，它能夠利用或叫用服務。 Sap 指出服務可供其他實體使用。
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: 'CIM_ServiceAccessPoint 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970203"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="ceb90-104">CIM_ServiceAccessPoint 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="ceb90-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="ceb90-105">代表 (SAP) 的服務存取點，它能夠利用或叫用服務。</span><span class="sxs-lookup"><span data-stu-id="ceb90-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="ceb90-106">Sap 指出服務可供其他實體使用。</span><span class="sxs-lookup"><span data-stu-id="ceb90-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb90-107">語法</span><span class="sxs-lookup"><span data-stu-id="ceb90-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="ceb90-108">成員</span><span class="sxs-lookup"><span data-stu-id="ceb90-108">Members</span></span>

<span data-ttu-id="ceb90-109">**CIM \_ ServiceAccessPoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ceb90-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="ceb90-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ceb90-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ceb90-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ceb90-111">Properties</span></span>

<span data-ttu-id="ceb90-112">**CIM \_ ServiceAccessPoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ceb90-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ceb90-113">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ceb90-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb90-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ceb90-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb90-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ceb90-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ceb90-117">用來建立這個類別之實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="ceb90-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="ceb90-118">**CreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別和其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ceb90-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="ceb90-119">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ceb90-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb90-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ceb90-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb90-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-122">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ceb90-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ceb90-123">SAP 的唯一名稱，表示 SAP 所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="ceb90-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="ceb90-124">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ceb90-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb90-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ceb90-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb90-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-127">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="ceb90-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="ceb90-128">用來建立包含 SAP 之系統實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="ceb90-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="ceb90-129">**SystemCreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別及其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ceb90-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="ceb90-130">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ceb90-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceb90-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ceb90-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb90-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceb90-133">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="ceb90-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="ceb90-134">包含 SAP 的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="ceb90-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ceb90-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ceb90-135">Requirements</span></span>



| <span data-ttu-id="ceb90-136">需求</span><span class="sxs-lookup"><span data-stu-id="ceb90-136">Requirement</span></span> | <span data-ttu-id="ceb90-137">值</span><span class="sxs-lookup"><span data-stu-id="ceb90-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb90-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ceb90-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb90-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ceb90-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ceb90-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ceb90-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb90-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ceb90-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ceb90-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="ceb90-142">Namespace</span></span><br/>                | <span data-ttu-id="ceb90-143">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ceb90-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ceb90-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ceb90-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceb90-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ceb90-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceb90-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ceb90-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceb90-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ceb90-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ceb90-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ceb90-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb90-149">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="ceb90-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

