---
description: 表示通訊協定端點相依于轉送服務以轉送資料的關聯。
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: CIM_ForwardsAmong 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985597"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="365e0-103">CIM \_ ForwardsAmong 類別</span><span class="sxs-lookup"><span data-stu-id="365e0-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="365e0-104">表示通訊協定端點相依于轉送服務以轉送資料的關聯。</span><span class="sxs-lookup"><span data-stu-id="365e0-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="365e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="365e0-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="365e0-106">成員</span><span class="sxs-lookup"><span data-stu-id="365e0-106">Members</span></span>

<span data-ttu-id="365e0-107">**CIM \_ ForwardsAmong** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="365e0-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="365e0-108">屬性</span><span class="sxs-lookup"><span data-stu-id="365e0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="365e0-109">屬性</span><span class="sxs-lookup"><span data-stu-id="365e0-109">Properties</span></span>

<span data-ttu-id="365e0-110">**CIM \_ ForwardsAmong** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="365e0-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="365e0-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="365e0-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365e0-112">資料類型： **CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="365e0-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="365e0-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="365e0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365e0-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="365e0-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="365e0-115">通訊協定端點會傳送和接收轉送的資料。</span><span class="sxs-lookup"><span data-stu-id="365e0-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="365e0-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="365e0-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365e0-117">資料類型： **CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="365e0-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="365e0-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="365e0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365e0-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="365e0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="365e0-120">轉送資料的轉送服務。</span><span class="sxs-lookup"><span data-stu-id="365e0-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="365e0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="365e0-121">Requirements</span></span>



| <span data-ttu-id="365e0-122">需求</span><span class="sxs-lookup"><span data-stu-id="365e0-122">Requirement</span></span> | <span data-ttu-id="365e0-123">值</span><span class="sxs-lookup"><span data-stu-id="365e0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="365e0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="365e0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="365e0-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="365e0-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="365e0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="365e0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="365e0-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="365e0-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="365e0-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="365e0-128">Namespace</span></span><br/>                | <span data-ttu-id="365e0-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="365e0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="365e0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="365e0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="365e0-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="365e0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="365e0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="365e0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="365e0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="365e0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="365e0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="365e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365e0-135">**CIM \_ ServiceSAPDependency**</span><span class="sxs-lookup"><span data-stu-id="365e0-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

