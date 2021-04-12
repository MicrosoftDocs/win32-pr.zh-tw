---
description: 代表來賓 VSS 服務。 它是用來查詢來自 Hyper-v 主機的來賓叢集資訊。
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Msvm_VssService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318084"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="b35c6-104">Msvm \_ VssService 類別</span><span class="sxs-lookup"><span data-stu-id="b35c6-104">Msvm\_VssService class</span></span>

<span data-ttu-id="b35c6-105">代表來賓 VSS 服務。</span><span class="sxs-lookup"><span data-stu-id="b35c6-105">Represents the guest VSS service.</span></span> <span data-ttu-id="b35c6-106">它是用來查詢來自 Hyper-v 主機的來賓叢集資訊。</span><span class="sxs-lookup"><span data-stu-id="b35c6-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="b35c6-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b35c6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35c6-108">語法</span><span class="sxs-lookup"><span data-stu-id="b35c6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="b35c6-109">成員</span><span class="sxs-lookup"><span data-stu-id="b35c6-109">Members</span></span>

<span data-ttu-id="b35c6-110">**Msvm \_ VssService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b35c6-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="b35c6-111">方法</span><span class="sxs-lookup"><span data-stu-id="b35c6-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b35c6-112">方法</span><span class="sxs-lookup"><span data-stu-id="b35c6-112">Methods</span></span>

<span data-ttu-id="b35c6-113">**Msvm \_ VssService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b35c6-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="b35c6-114">方法</span><span class="sxs-lookup"><span data-stu-id="b35c6-114">Method</span></span>                                                                               | <span data-ttu-id="b35c6-115">描述</span><span class="sxs-lookup"><span data-stu-id="b35c6-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="b35c6-116">**QueryGuestClusterInformation**</span><span class="sxs-lookup"><span data-stu-id="b35c6-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="b35c6-117">查詢從 Hyper-v 主機到來賓的叢集資訊。</span><span class="sxs-lookup"><span data-stu-id="b35c6-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b35c6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b35c6-118">Requirements</span></span>



| <span data-ttu-id="b35c6-119">需求</span><span class="sxs-lookup"><span data-stu-id="b35c6-119">Requirement</span></span> | <span data-ttu-id="b35c6-120">值</span><span class="sxs-lookup"><span data-stu-id="b35c6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35c6-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b35c6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b35c6-122">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b35c6-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b35c6-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b35c6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b35c6-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b35c6-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b35c6-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="b35c6-125">Namespace</span></span><br/>                | <span data-ttu-id="b35c6-126">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b35c6-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b35c6-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b35c6-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b35c6-128"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b35c6-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b35c6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b35c6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b35c6-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b35c6-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b35c6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b35c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35c6-132">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="b35c6-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




