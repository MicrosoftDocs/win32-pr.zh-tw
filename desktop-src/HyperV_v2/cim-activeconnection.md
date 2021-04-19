---
description: 定義目前開啟並設定的連接，以提供兩個 CIM ServiceAccessPoint 物件之間的通訊 \_ 。
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: CIM_ActiveConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969238"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="43f53-103">CIM \_ ActiveConnection 類別</span><span class="sxs-lookup"><span data-stu-id="43f53-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="43f53-104">定義目前開啟並設定的連接，以提供兩個 **CIM \_ ServiceAccessPoint** 物件之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="43f53-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="43f53-105">**CIM \_** 當連接未被視為 **CIM \_ ManagedElement** 物件時，會使用 ActiveConnection。</span><span class="sxs-lookup"><span data-stu-id="43f53-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="43f53-106">使用中連接所連接的服務存取點通常位於相同的網路或應用層。</span><span class="sxs-lookup"><span data-stu-id="43f53-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f53-107">語法</span><span class="sxs-lookup"><span data-stu-id="43f53-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="43f53-108">成員</span><span class="sxs-lookup"><span data-stu-id="43f53-108">Members</span></span>

<span data-ttu-id="43f53-109">**CIM \_ ActiveConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="43f53-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="43f53-110">屬性</span><span class="sxs-lookup"><span data-stu-id="43f53-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43f53-111">屬性</span><span class="sxs-lookup"><span data-stu-id="43f53-111">Properties</span></span>

<span data-ttu-id="43f53-112">**CIM \_ ActiveConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="43f53-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43f53-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="43f53-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f53-114">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="43f53-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="43f53-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43f53-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f53-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="43f53-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="43f53-117">透過使用中連線連接到其他服務存取點的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="43f53-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="43f53-118">**CIM \_ServiceAccessPoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="43f53-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="43f53-119">在單向連接中，此存取點是傳輸資料的存取點。</span><span class="sxs-lookup"><span data-stu-id="43f53-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="43f53-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="43f53-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f53-121">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="43f53-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="43f53-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43f53-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f53-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="43f53-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="43f53-124">設定為通訊或正在主動與 **Antecedent** 屬性中指定之服務存取點通訊的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="43f53-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="43f53-125">在單向連接中，此存取點是接收資料的存取點。</span><span class="sxs-lookup"><span data-stu-id="43f53-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="43f53-126">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="43f53-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f53-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="43f53-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43f53-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43f53-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43f53-129">如果連接是單向的，則為 True;如果連接是雙向的，則為 false。</span><span class="sxs-lookup"><span data-stu-id="43f53-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="43f53-130">當連接為單向時， **Antecedent** 屬性會指定傳輸資料的存取點。</span><span class="sxs-lookup"><span data-stu-id="43f53-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="43f53-131">在雙向連接中， **Antecedent** 可以指定指派給連接的存取點。</span><span class="sxs-lookup"><span data-stu-id="43f53-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="43f53-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="43f53-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f53-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43f53-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43f53-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43f53-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f53-135">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "No value" ) ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ActiveConnection**。**TrafficType**") </span><span class="sxs-lookup"><span data-stu-id="43f53-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="43f53-136">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="43f53-136">This property is deprecated.</span></span> <span data-ttu-id="43f53-137">相反地，我們建議您在端點的定址、通訊協定和基本功能中指定這項資訊。</span><span class="sxs-lookup"><span data-stu-id="43f53-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="43f53-138">當 **TrafficType** 屬性設定為 "1" (其他) 時所指定的流量類型描述。</span><span class="sxs-lookup"><span data-stu-id="43f53-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="43f53-139">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="43f53-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43f53-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43f53-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43f53-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43f53-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43f53-142">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ ActiveConnection**。**OtherTrafficDescription**") </span><span class="sxs-lookup"><span data-stu-id="43f53-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="43f53-143">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="43f53-143">This property is deprecated.</span></span> <span data-ttu-id="43f53-144">相反地，我們建議您在端點的定址、通訊協定和基本功能中指定這項資訊。</span><span class="sxs-lookup"><span data-stu-id="43f53-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="43f53-145">透過此連接傳輸的流量類型。</span><span class="sxs-lookup"><span data-stu-id="43f53-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43f53-146">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="43f53-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43f53-147">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="43f53-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="43f53-148">**單播** (2) </span><span class="sxs-lookup"><span data-stu-id="43f53-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="43f53-149">**廣播** (3) </span><span class="sxs-lookup"><span data-stu-id="43f53-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="43f53-150">**多播** (4) </span><span class="sxs-lookup"><span data-stu-id="43f53-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="43f53-151">**任意** 傳播 (5) </span><span class="sxs-lookup"><span data-stu-id="43f53-151">**Anycast** (5)</span></span>


<span data-ttu-id="43f53-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="43f53-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="43f53-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="43f53-153">Requirements</span></span>



| <span data-ttu-id="43f53-154">需求</span><span class="sxs-lookup"><span data-stu-id="43f53-154">Requirement</span></span> | <span data-ttu-id="43f53-155">值</span><span class="sxs-lookup"><span data-stu-id="43f53-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f53-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43f53-156">Minimum supported client</span></span><br/> | <span data-ttu-id="43f53-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="43f53-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="43f53-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43f53-158">Minimum supported server</span></span><br/> | <span data-ttu-id="43f53-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="43f53-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="43f53-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="43f53-160">Namespace</span></span><br/>                | <span data-ttu-id="43f53-161">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="43f53-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="43f53-162">MOF</span><span class="sxs-lookup"><span data-stu-id="43f53-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43f53-163"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="43f53-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43f53-164">DLL</span><span class="sxs-lookup"><span data-stu-id="43f53-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43f53-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43f53-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43f53-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43f53-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f53-167">**CIM \_ SAPSAPDependency**</span><span class="sxs-lookup"><span data-stu-id="43f53-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

