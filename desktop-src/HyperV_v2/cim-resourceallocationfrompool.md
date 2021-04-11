---
description: 表示從資源集區配置 CIM \_ ResourceAllocationSettingData 實例的關聯。
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: CIM_ResourceAllocationFromPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944770"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="b4341-103">CIM \_ ResourceAllocationFromPool 類別</span><span class="sxs-lookup"><span data-stu-id="b4341-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="b4341-104">表示從資源集區配置 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例的關聯。</span><span class="sxs-lookup"><span data-stu-id="b4341-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4341-105">語法</span><span class="sxs-lookup"><span data-stu-id="b4341-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b4341-106">成員</span><span class="sxs-lookup"><span data-stu-id="b4341-106">Members</span></span>

<span data-ttu-id="b4341-107">**CIM \_ ResourceAllocationFromPool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b4341-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="b4341-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b4341-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4341-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b4341-109">Properties</span></span>

<span data-ttu-id="b4341-110">**CIM \_ ResourceAllocationFromPool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b4341-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4341-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="b4341-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4341-112">資料類型： **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="b4341-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="b4341-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b4341-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4341-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="b4341-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b4341-115">資源集區。</span><span class="sxs-lookup"><span data-stu-id="b4341-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="b4341-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b4341-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4341-117">資料類型： **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="b4341-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="b4341-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b4341-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4341-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="b4341-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b4341-120">資源配置資料。</span><span class="sxs-lookup"><span data-stu-id="b4341-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4341-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4341-121">Requirements</span></span>



| <span data-ttu-id="b4341-122">需求</span><span class="sxs-lookup"><span data-stu-id="b4341-122">Requirement</span></span> | <span data-ttu-id="b4341-123">值</span><span class="sxs-lookup"><span data-stu-id="b4341-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4341-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4341-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b4341-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b4341-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b4341-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4341-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b4341-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4341-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b4341-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="b4341-128">Namespace</span></span><br/>                | <span data-ttu-id="b4341-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b4341-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b4341-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b4341-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4341-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b4341-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4341-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b4341-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4341-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4341-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b4341-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4341-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4341-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="b4341-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

