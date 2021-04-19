---
description: 代表服務存取點 (SAP) 和執行它的邏輯裝置之間的關聯。
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: 'CIM_DeviceSAPImplementation 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966763"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="e6d2f-103">CIM_DeviceSAPImplementation 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="e6d2f-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="e6d2f-104">代表服務存取點 (SAP) 和執行它的邏輯裝置之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="e6d2f-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6d2f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e6d2f-106">成員</span><span class="sxs-lookup"><span data-stu-id="e6d2f-106">Members</span></span>

<span data-ttu-id="e6d2f-107">**CIM \_ DeviceSAPImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e6d2f-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="e6d2f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e6d2f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6d2f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e6d2f-109">Properties</span></span>

<span data-ttu-id="e6d2f-110">**CIM \_ DeviceSAPImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e6d2f-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6d2f-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="e6d2f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d2f-112">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e6d2f-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e6d2f-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d2f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d2f-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="e6d2f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e6d2f-115">邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="e6d2f-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="e6d2f-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="e6d2f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6d2f-117">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="e6d2f-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="e6d2f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e6d2f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6d2f-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="e6d2f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e6d2f-120">邏輯裝置所執行的 SAP。</span><span class="sxs-lookup"><span data-stu-id="e6d2f-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6d2f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6d2f-121">Requirements</span></span>



| <span data-ttu-id="e6d2f-122">需求</span><span class="sxs-lookup"><span data-stu-id="e6d2f-122">Requirement</span></span> | <span data-ttu-id="e6d2f-123">值</span><span class="sxs-lookup"><span data-stu-id="e6d2f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d2f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6d2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d2f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6d2f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e6d2f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6d2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d2f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6d2f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e6d2f-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="e6d2f-128">Namespace</span></span><br/>                | <span data-ttu-id="e6d2f-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6d2f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e6d2f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e6d2f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6d2f-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e6d2f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6d2f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d2f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6d2f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6d2f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6d2f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6d2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d2f-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="e6d2f-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

