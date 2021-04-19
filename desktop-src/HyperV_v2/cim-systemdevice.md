---
description: 將系統與系統元件的邏輯裝置產生關聯。
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: 'CIM_SystemDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982365"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="4a4b7-103">CIM_SystemDevice 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="4a4b7-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="4a4b7-104">將系統與系統元件的邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a4b7-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a4b7-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4a4b7-106">成員</span><span class="sxs-lookup"><span data-stu-id="4a4b7-106">Members</span></span>

<span data-ttu-id="4a4b7-107">**CIM \_ SystemDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4a4b7-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4a4b7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="4a4b7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a4b7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4a4b7-109">Properties</span></span>

<span data-ttu-id="4a4b7-110">**CIM \_ SystemDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4a4b7-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a4b7-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4a4b7-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4b7-112">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="4a4b7-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="4a4b7-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4b7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4b7-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="4a4b7-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4a4b7-115">關聯中父系統的 [**CIM \_ 系統**](cim-system.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="4a4b7-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="4a4b7-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4a4b7-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4b7-117">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="4a4b7-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4a4b7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a4b7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4b7-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="4a4b7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a4b7-120">屬於系統元件之邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="4a4b7-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a4b7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a4b7-121">Requirements</span></span>



| <span data-ttu-id="4a4b7-122">需求</span><span class="sxs-lookup"><span data-stu-id="4a4b7-122">Requirement</span></span> | <span data-ttu-id="4a4b7-123">值</span><span class="sxs-lookup"><span data-stu-id="4a4b7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4b7-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a4b7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4b7-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4a4b7-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4a4b7-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a4b7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4b7-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a4b7-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4a4b7-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="4a4b7-128">Namespace</span></span><br/>                | <span data-ttu-id="4a4b7-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a4b7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4a4b7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4a4b7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a4b7-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a4b7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4a4b7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a4b7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a4b7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a4b7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a4b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4b7-135">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="4a4b7-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

