---
description: 表示兩個或多個裝置已連接在一起的關聯性。
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: 'CIM_DeviceConnection 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973885"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="a2a17-103">CIM_DeviceConnection 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="a2a17-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="a2a17-104">表示兩個或多個裝置已連接在一起的關聯性。</span><span class="sxs-lookup"><span data-stu-id="a2a17-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a17-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2a17-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="a2a17-106">成員</span><span class="sxs-lookup"><span data-stu-id="a2a17-106">Members</span></span>

<span data-ttu-id="a2a17-107">**CIM \_ DeviceConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a2a17-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="a2a17-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a2a17-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2a17-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a2a17-109">Properties</span></span>

<span data-ttu-id="a2a17-110">**CIM \_ DeviceConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a2a17-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2a17-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="a2a17-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2a17-112">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a2a17-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2a17-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="a2a17-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a2a17-115">裝置。</span><span class="sxs-lookup"><span data-stu-id="a2a17-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="a2a17-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="a2a17-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2a17-117">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a2a17-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2a17-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="a2a17-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a2a17-120">連線到其他裝置的第二個裝置。</span><span class="sxs-lookup"><span data-stu-id="a2a17-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="a2a17-121">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="a2a17-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2a17-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2a17-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2a17-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-124">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bits" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠關聯 \| 001.3 ") ， **PUnit** (" bit ") </span><span class="sxs-lookup"><span data-stu-id="a2a17-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="a2a17-125">當有數個匯流排和連接資料的寬度時，NegotiatedDataWidth 屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="a2a17-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="a2a17-126">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="a2a17-126">Data width is specified in bits.</span></span> <span data-ttu-id="a2a17-127">如果資料寬度未經過協商，或此資訊無法使用或對裝置管理而言不重要，則應該將屬性設定為0。</span><span class="sxs-lookup"><span data-stu-id="a2a17-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2a17-128">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="a2a17-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2a17-129">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a2a17-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2a17-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2a17-131">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 匯流排埠關聯 \| 001.2 ") ， **PUnit** (" bit/second ") </span><span class="sxs-lookup"><span data-stu-id="a2a17-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="a2a17-132">當有數個匯流排和連線速度可供使用時，此屬性會定義裝置之間使用的速度（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2a17-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="a2a17-133">如果未協商連線或匯流排速度，或此資訊無法使用，或對裝置管理而言不重要，則應該將屬性設定為 "0"。</span><span class="sxs-lookup"><span data-stu-id="a2a17-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2a17-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2a17-134">Requirements</span></span>



| <span data-ttu-id="a2a17-135">需求</span><span class="sxs-lookup"><span data-stu-id="a2a17-135">Requirement</span></span> | <span data-ttu-id="a2a17-136">值</span><span class="sxs-lookup"><span data-stu-id="a2a17-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a17-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2a17-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a17-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2a17-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a2a17-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2a17-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a17-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2a17-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a2a17-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2a17-141">Namespace</span></span><br/>                | <span data-ttu-id="a2a17-142">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2a17-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2a17-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a2a17-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2a17-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a2a17-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2a17-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a2a17-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2a17-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2a17-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2a17-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2a17-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a17-148">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="a2a17-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

