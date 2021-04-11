---
description: 表示一種關聯，其中服務是父項服務的元件，這兩者會形成較高層級的服務。
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: CIM_ServiceComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191492"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="b4cd7-103">CIM \_ ServiceComponent 類別</span><span class="sxs-lookup"><span data-stu-id="b4cd7-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="b4cd7-104">表示一種關聯，其中服務是父項服務的元件，這兩者會形成較高層級的服務。</span><span class="sxs-lookup"><span data-stu-id="b4cd7-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="b4cd7-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b4cd7-106">成員</span><span class="sxs-lookup"><span data-stu-id="b4cd7-106">Members</span></span>

<span data-ttu-id="b4cd7-107">**CIM \_ ServiceComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b4cd7-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b4cd7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b4cd7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4cd7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b4cd7-109">Properties</span></span>

<span data-ttu-id="b4cd7-110">**CIM \_ ServiceComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b4cd7-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4cd7-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b4cd7-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cd7-112">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="b4cd7-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="b4cd7-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b4cd7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cd7-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="b4cd7-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b4cd7-115">父項服務。</span><span class="sxs-lookup"><span data-stu-id="b4cd7-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="b4cd7-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b4cd7-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4cd7-117">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="b4cd7-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="b4cd7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b4cd7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4cd7-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="b4cd7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b4cd7-120">元件服務。</span><span class="sxs-lookup"><span data-stu-id="b4cd7-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4cd7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4cd7-121">Requirements</span></span>



| <span data-ttu-id="b4cd7-122">需求</span><span class="sxs-lookup"><span data-stu-id="b4cd7-122">Requirement</span></span> | <span data-ttu-id="b4cd7-123">值</span><span class="sxs-lookup"><span data-stu-id="b4cd7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cd7-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4cd7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b4cd7-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b4cd7-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b4cd7-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4cd7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b4cd7-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b4cd7-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b4cd7-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="b4cd7-128">Namespace</span></span><br/>                | <span data-ttu-id="b4cd7-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b4cd7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b4cd7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b4cd7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4cd7-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b4cd7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4cd7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cd7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4cd7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4cd7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b4cd7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4cd7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cd7-135">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="b4cd7-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

