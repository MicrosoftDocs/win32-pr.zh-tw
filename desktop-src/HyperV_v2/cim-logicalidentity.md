---
description: 表示兩個 managed 專案之間的泛型關聯，這些元素代表相同基礎實體的不同層面。
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: 'CIM_LogicalIdentity 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970754"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="e24a3-103">CIM_LogicalIdentity 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="e24a3-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="e24a3-104">表示兩個 managed 專案之間的泛型關聯，這些元素代表相同基礎實體的不同層面。</span><span class="sxs-lookup"><span data-stu-id="e24a3-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="e24a3-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="e24a3-106">成員</span><span class="sxs-lookup"><span data-stu-id="e24a3-106">Members</span></span>

<span data-ttu-id="e24a3-107">**CIM \_ LogicalIdentity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e24a3-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="e24a3-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e24a3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e24a3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e24a3-109">Properties</span></span>

<span data-ttu-id="e24a3-110">**CIM \_ LogicalIdentity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e24a3-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e24a3-111">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="e24a3-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24a3-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e24a3-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="e24a3-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e24a3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e24a3-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e24a3-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e24a3-115">關聯中的第二個方面。</span><span class="sxs-lookup"><span data-stu-id="e24a3-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="e24a3-116">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="e24a3-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24a3-117">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e24a3-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="e24a3-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e24a3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e24a3-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e24a3-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e24a3-120">關聯中的第一個方面。</span><span class="sxs-lookup"><span data-stu-id="e24a3-120">The first aspect in the association.</span></span> <span data-ttu-id="e24a3-121">在屬性名稱中使用系統不會限制關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="e24a3-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e24a3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e24a3-122">Requirements</span></span>



| <span data-ttu-id="e24a3-123">需求</span><span class="sxs-lookup"><span data-stu-id="e24a3-123">Requirement</span></span> | <span data-ttu-id="e24a3-124">值</span><span class="sxs-lookup"><span data-stu-id="e24a3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e24a3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e24a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e24a3-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e24a3-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e24a3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e24a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e24a3-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e24a3-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e24a3-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="e24a3-129">Namespace</span></span><br/>                | <span data-ttu-id="e24a3-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e24a3-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e24a3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e24a3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e24a3-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e24a3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e24a3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e24a3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e24a3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e24a3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

