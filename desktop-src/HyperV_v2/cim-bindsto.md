---
description: 代表 CIM \_ ServiceAccessPoint 物件從 cim ProtocolEndpoint 物件要求通訊協定服務的關聯 \_ 。
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: CIM_BindsTo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978200"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="793be-103">CIM \_ BindsTo 類別</span><span class="sxs-lookup"><span data-stu-id="793be-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="793be-104">代表 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 物件從 [**cim \_ ProtocolEndpoint**](cim-protocolendpoint.md) 物件要求通訊協定服務的關聯。</span><span class="sxs-lookup"><span data-stu-id="793be-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="793be-105">語法</span><span class="sxs-lookup"><span data-stu-id="793be-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="793be-106">成員</span><span class="sxs-lookup"><span data-stu-id="793be-106">Members</span></span>

<span data-ttu-id="793be-107">**CIM \_ BindsTo** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="793be-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="793be-108">屬性</span><span class="sxs-lookup"><span data-stu-id="793be-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="793be-109">屬性</span><span class="sxs-lookup"><span data-stu-id="793be-109">Properties</span></span>

<span data-ttu-id="793be-110">**CIM \_ BindsTo** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="793be-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="793be-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="793be-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793be-112">資料類型： **CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="793be-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="793be-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="793be-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793be-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="793be-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="793be-115">服務存取點所存取的較低層級端點。</span><span class="sxs-lookup"><span data-stu-id="793be-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="793be-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="793be-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793be-117">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="793be-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="793be-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="793be-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793be-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="793be-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="793be-120">相依于較低層級端點的存取點或通訊協定端點。</span><span class="sxs-lookup"><span data-stu-id="793be-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="793be-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="793be-121">Requirements</span></span>



| <span data-ttu-id="793be-122">需求</span><span class="sxs-lookup"><span data-stu-id="793be-122">Requirement</span></span> | <span data-ttu-id="793be-123">值</span><span class="sxs-lookup"><span data-stu-id="793be-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="793be-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="793be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="793be-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="793be-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="793be-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="793be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="793be-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="793be-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="793be-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="793be-128">Namespace</span></span><br/>                | <span data-ttu-id="793be-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="793be-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="793be-130">MOF</span><span class="sxs-lookup"><span data-stu-id="793be-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="793be-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="793be-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="793be-132">DLL</span><span class="sxs-lookup"><span data-stu-id="793be-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="793be-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="793be-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="793be-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="793be-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793be-135">**CIM \_ SAPSAPDependency**</span><span class="sxs-lookup"><span data-stu-id="793be-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

