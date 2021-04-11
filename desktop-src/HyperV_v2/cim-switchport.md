---
description: 代表傳送和接收資料框架的切換埠。
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: CIM_SwitchPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944298"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="61a19-103">CIM \_ 交換器類別</span><span class="sxs-lookup"><span data-stu-id="61a19-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="61a19-104">代表傳送和接收資料框架的切換埠。</span><span class="sxs-lookup"><span data-stu-id="61a19-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a19-105">語法</span><span class="sxs-lookup"><span data-stu-id="61a19-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="61a19-106">成員</span><span class="sxs-lookup"><span data-stu-id="61a19-106">Members</span></span>

<span data-ttu-id="61a19-107">**CIM \_ 交換器** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="61a19-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="61a19-108">屬性</span><span class="sxs-lookup"><span data-stu-id="61a19-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61a19-109">屬性</span><span class="sxs-lookup"><span data-stu-id="61a19-109">Properties</span></span>

<span data-ttu-id="61a19-110">**CIM \_ 交換器** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="61a19-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61a19-111">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="61a19-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a19-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="61a19-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a19-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61a19-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a19-114">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| BRIDGE-dot1dPort ") </span><span class="sxs-lookup"><span data-stu-id="61a19-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="61a19-115">交換器埠的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="61a19-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61a19-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="61a19-116">Requirements</span></span>



| <span data-ttu-id="61a19-117">需求</span><span class="sxs-lookup"><span data-stu-id="61a19-117">Requirement</span></span> | <span data-ttu-id="61a19-118">值</span><span class="sxs-lookup"><span data-stu-id="61a19-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a19-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61a19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="61a19-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="61a19-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="61a19-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61a19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="61a19-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="61a19-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="61a19-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="61a19-123">Namespace</span></span><br/>                | <span data-ttu-id="61a19-124">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="61a19-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61a19-125">MOF</span><span class="sxs-lookup"><span data-stu-id="61a19-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61a19-126"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="61a19-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61a19-127">DLL</span><span class="sxs-lookup"><span data-stu-id="61a19-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a19-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61a19-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61a19-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61a19-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a19-130">**CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="61a19-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

