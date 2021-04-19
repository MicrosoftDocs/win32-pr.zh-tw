---
description: 表示 managed 專案由另一個主控的關聯。
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: CIM_HostedDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973998"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="95034-103">CIM \_ HostedDependency 類別</span><span class="sxs-lookup"><span data-stu-id="95034-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="95034-104">表示 managed 專案由另一個主控的關聯。</span><span class="sxs-lookup"><span data-stu-id="95034-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="95034-105">語法</span><span class="sxs-lookup"><span data-stu-id="95034-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="95034-106">成員</span><span class="sxs-lookup"><span data-stu-id="95034-106">Members</span></span>

<span data-ttu-id="95034-107">**CIM \_ HostedDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="95034-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="95034-108">屬性</span><span class="sxs-lookup"><span data-stu-id="95034-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95034-109">屬性</span><span class="sxs-lookup"><span data-stu-id="95034-109">Properties</span></span>

<span data-ttu-id="95034-110">**CIM \_ HostedDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="95034-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95034-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="95034-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95034-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="95034-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="95034-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="95034-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95034-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="95034-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="95034-115">主機受管理的元素。</span><span class="sxs-lookup"><span data-stu-id="95034-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="95034-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="95034-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95034-117">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="95034-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="95034-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="95034-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95034-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="95034-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="95034-120">主控的 managed 專案。</span><span class="sxs-lookup"><span data-stu-id="95034-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95034-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="95034-121">Requirements</span></span>



| <span data-ttu-id="95034-122">需求</span><span class="sxs-lookup"><span data-stu-id="95034-122">Requirement</span></span> | <span data-ttu-id="95034-123">值</span><span class="sxs-lookup"><span data-stu-id="95034-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95034-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95034-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95034-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="95034-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="95034-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95034-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95034-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95034-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="95034-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="95034-128">Namespace</span></span><br/>                | <span data-ttu-id="95034-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="95034-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95034-130">MOF</span><span class="sxs-lookup"><span data-stu-id="95034-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95034-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="95034-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95034-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95034-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95034-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95034-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95034-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95034-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95034-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="95034-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

