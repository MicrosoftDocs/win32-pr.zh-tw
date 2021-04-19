---
description: 表示轉送資料庫中與 CIM TransparentBridgingService 類別相關聯的專案 \_ 。
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: CIM_DynamicForwardingEntry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972472"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="89a54-103">CIM \_ DynamicForwardingEntry 類別</span><span class="sxs-lookup"><span data-stu-id="89a54-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="89a54-104">表示轉送資料庫中與 [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) 類別相關聯的專案。</span><span class="sxs-lookup"><span data-stu-id="89a54-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a54-105">語法</span><span class="sxs-lookup"><span data-stu-id="89a54-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="89a54-106">成員</span><span class="sxs-lookup"><span data-stu-id="89a54-106">Members</span></span>

<span data-ttu-id="89a54-107">**CIM \_ DynamicForwardingEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89a54-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="89a54-108">屬性</span><span class="sxs-lookup"><span data-stu-id="89a54-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89a54-109">屬性</span><span class="sxs-lookup"><span data-stu-id="89a54-109">Properties</span></span>

<span data-ttu-id="89a54-110">**CIM \_ DynamicForwardingEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89a54-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89a54-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89a54-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89a54-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-114">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="89a54-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="89a54-115">類別的名稱，或用來建立實例的子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="89a54-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="89a54-116">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="89a54-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="89a54-117">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="89a54-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89a54-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-120">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| BRIDGE-dot1dTpFdbStatus ") </span><span class="sxs-lookup"><span data-stu-id="89a54-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="89a54-121">專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="89a54-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89a54-122">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="89a54-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="89a54-123">**無效** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="89a54-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="89a54-124">**學習** (3) </span><span class="sxs-lookup"><span data-stu-id="89a54-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="89a54-125">**Self** (4) </span><span class="sxs-lookup"><span data-stu-id="89a54-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="89a54-126">**管理** (5) </span><span class="sxs-lookup"><span data-stu-id="89a54-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89a54-127">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="89a54-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89a54-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-130">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| BRIDGE-dot1dTpFdbAddress ") </span><span class="sxs-lookup"><span data-stu-id="89a54-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="89a54-131">橋接服務用來篩選資訊的單播 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="89a54-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="89a54-132">MAC 位址的格式為12個十六進位數位（例如010203040506），每一組都代表根據 RFC 2469 的標準位順序中，其中一個 MAC 位址的六個八位。</span><span class="sxs-lookup"><span data-stu-id="89a54-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="89a54-133">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89a54-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89a54-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-136">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 服務**](cim-service.md)」。**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="89a54-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="89a54-137">範圍服務物件的 **CreationClassName** 值。</span><span class="sxs-lookup"><span data-stu-id="89a54-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="89a54-138">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="89a54-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89a54-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-141">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 服務**](cim-service.md)」。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="89a54-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="89a54-142">範圍服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="89a54-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="89a54-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89a54-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89a54-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-146">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="89a54-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="89a54-147">範圍系統物件的 **CreationClassName** 值。</span><span class="sxs-lookup"><span data-stu-id="89a54-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="89a54-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="89a54-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89a54-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89a54-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89a54-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89a54-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89a54-151">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="89a54-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="89a54-152">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="89a54-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89a54-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="89a54-153">Requirements</span></span>



| <span data-ttu-id="89a54-154">需求</span><span class="sxs-lookup"><span data-stu-id="89a54-154">Requirement</span></span> | <span data-ttu-id="89a54-155">值</span><span class="sxs-lookup"><span data-stu-id="89a54-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a54-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89a54-156">Minimum supported client</span></span><br/> | <span data-ttu-id="89a54-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="89a54-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="89a54-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89a54-158">Minimum supported server</span></span><br/> | <span data-ttu-id="89a54-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89a54-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="89a54-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="89a54-160">Namespace</span></span><br/>                | <span data-ttu-id="89a54-161">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="89a54-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="89a54-162">MOF</span><span class="sxs-lookup"><span data-stu-id="89a54-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89a54-163"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="89a54-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89a54-164">DLL</span><span class="sxs-lookup"><span data-stu-id="89a54-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89a54-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89a54-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89a54-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89a54-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a54-167">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="89a54-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

