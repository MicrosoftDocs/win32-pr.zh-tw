---
description: 表示作業與負責建立作業的 managed 元素之間的關聯。
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Msvm_OwningJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994538"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="2678b-103">Msvm \_ OwningJobElement 類別</span><span class="sxs-lookup"><span data-stu-id="2678b-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="2678b-104">表示作業與負責建立作業的 managed 元素之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="2678b-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="2678b-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2678b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2678b-106">語法</span><span class="sxs-lookup"><span data-stu-id="2678b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="2678b-107">成員</span><span class="sxs-lookup"><span data-stu-id="2678b-107">Members</span></span>

<span data-ttu-id="2678b-108">**Msvm \_ OwningJobElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2678b-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="2678b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2678b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2678b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2678b-110">Properties</span></span>

<span data-ttu-id="2678b-111">**Msvm \_ OwningJobElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2678b-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2678b-112">**OwnedElement**</span><span class="sxs-lookup"><span data-stu-id="2678b-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2678b-113">資料類型： **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="2678b-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2678b-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2678b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2678b-115">Managed 元素所建立的作業。</span><span class="sxs-lookup"><span data-stu-id="2678b-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="2678b-116">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="2678b-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2678b-117">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2678b-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2678b-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2678b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2678b-119">負責建立作業的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="2678b-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2678b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2678b-120">Requirements</span></span>



| <span data-ttu-id="2678b-121">需求</span><span class="sxs-lookup"><span data-stu-id="2678b-121">Requirement</span></span> | <span data-ttu-id="2678b-122">值</span><span class="sxs-lookup"><span data-stu-id="2678b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2678b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2678b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2678b-124">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2678b-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2678b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2678b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2678b-126">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2678b-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2678b-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="2678b-127">Namespace</span></span><br/>                | <span data-ttu-id="2678b-128">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2678b-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2678b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2678b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2678b-130"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2678b-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2678b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2678b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2678b-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2678b-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

