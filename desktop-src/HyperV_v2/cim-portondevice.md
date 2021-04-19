---
description: 表示埠或連接點與裝置之間的關聯。
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: CIM_PortOnDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986651"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="6ccab-103">CIM \_ PortOnDevice 類別</span><span class="sxs-lookup"><span data-stu-id="6ccab-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="6ccab-104">表示埠或連接點與裝置之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="6ccab-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccab-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ccab-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6ccab-106">成員</span><span class="sxs-lookup"><span data-stu-id="6ccab-106">Members</span></span>

<span data-ttu-id="6ccab-107">**CIM \_ PortOnDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6ccab-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="6ccab-108">屬性</span><span class="sxs-lookup"><span data-stu-id="6ccab-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ccab-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6ccab-109">Properties</span></span>

<span data-ttu-id="6ccab-110">**CIM \_ PortOnDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6ccab-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ccab-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="6ccab-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ccab-112">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="6ccab-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6ccab-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ccab-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ccab-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="6ccab-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6ccab-115">包含埠的裝置。</span><span class="sxs-lookup"><span data-stu-id="6ccab-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="6ccab-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6ccab-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ccab-117">資料類型： **CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="6ccab-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="6ccab-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ccab-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ccab-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="6ccab-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6ccab-120">裝置上的埠。</span><span class="sxs-lookup"><span data-stu-id="6ccab-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ccab-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ccab-121">Requirements</span></span>



| <span data-ttu-id="6ccab-122">需求</span><span class="sxs-lookup"><span data-stu-id="6ccab-122">Requirement</span></span> | <span data-ttu-id="6ccab-123">值</span><span class="sxs-lookup"><span data-stu-id="6ccab-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccab-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ccab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccab-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6ccab-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6ccab-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ccab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccab-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ccab-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6ccab-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ccab-128">Namespace</span></span><br/>                | <span data-ttu-id="6ccab-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6ccab-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ccab-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6ccab-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ccab-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6ccab-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ccab-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6ccab-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ccab-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ccab-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ccab-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ccab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccab-135">**CIM \_ HostedDependency**</span><span class="sxs-lookup"><span data-stu-id="6ccab-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

