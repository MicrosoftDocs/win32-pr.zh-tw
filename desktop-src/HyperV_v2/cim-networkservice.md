---
description: 這個類別已被取代。 相反地，我們建議從 CIM \_ 服務類別衍生。
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979825"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="89de2-104">CIM \_ NetworkService 類別</span><span class="sxs-lookup"><span data-stu-id="89de2-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="89de2-105">這個類別已被取代。</span><span class="sxs-lookup"><span data-stu-id="89de2-105">This class is deprecated.</span></span> <span data-ttu-id="89de2-106">相反地，我們建議從 [**CIM \_ 服務**](cim-service.md) 類別衍生。</span><span class="sxs-lookup"><span data-stu-id="89de2-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="89de2-107">語法</span><span class="sxs-lookup"><span data-stu-id="89de2-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="89de2-108">成員</span><span class="sxs-lookup"><span data-stu-id="89de2-108">Members</span></span>

<span data-ttu-id="89de2-109">**CIM \_ NetworkService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89de2-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="89de2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="89de2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89de2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="89de2-111">Properties</span></span>

<span data-ttu-id="89de2-112">**CIM \_ NetworkService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89de2-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89de2-113">**關鍵字**</span><span class="sxs-lookup"><span data-stu-id="89de2-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89de2-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89de2-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89de2-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89de2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89de2-116">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) </span><span class="sxs-lookup"><span data-stu-id="89de2-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="89de2-117">此屬性已過時而不應使用。</span><span class="sxs-lookup"><span data-stu-id="89de2-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="89de2-118">已淘汰的描述：可在查詢中使用的關鍵字陣列。</span><span class="sxs-lookup"><span data-stu-id="89de2-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="89de2-119">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="89de2-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89de2-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89de2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89de2-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89de2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89de2-122">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ ServiceAccessURI" ) </span><span class="sxs-lookup"><span data-stu-id="89de2-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="89de2-123">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="89de2-123">This property is deprecated.</span></span> <span data-ttu-id="89de2-124">相反地，我們建議 **CIM \_ ServiceAccessURI** 類別。</span><span class="sxs-lookup"><span data-stu-id="89de2-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="89de2-125">已淘汰的描述：提供存取服務所需的通訊協定、網路位置和其他服務特定資訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="89de2-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="89de2-126">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="89de2-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89de2-127">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89de2-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89de2-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89de2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89de2-129">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) </span><span class="sxs-lookup"><span data-stu-id="89de2-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="89de2-130">此屬性已過時而不應使用。</span><span class="sxs-lookup"><span data-stu-id="89de2-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="89de2-131">已淘汰的描述：必須符合才能讓此服務正確啟動的前置條件。</span><span class="sxs-lookup"><span data-stu-id="89de2-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="89de2-132">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="89de2-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89de2-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89de2-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89de2-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89de2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89de2-135">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) </span><span class="sxs-lookup"><span data-stu-id="89de2-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="89de2-136">此屬性已過時而不應使用。</span><span class="sxs-lookup"><span data-stu-id="89de2-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="89de2-137">已淘汰的描述：必須提供給 **StartService** 方法的參數，才能讓此服務正確啟動。</span><span class="sxs-lookup"><span data-stu-id="89de2-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89de2-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="89de2-138">Requirements</span></span>



| <span data-ttu-id="89de2-139">需求</span><span class="sxs-lookup"><span data-stu-id="89de2-139">Requirement</span></span> | <span data-ttu-id="89de2-140">值</span><span class="sxs-lookup"><span data-stu-id="89de2-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89de2-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89de2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="89de2-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="89de2-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="89de2-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89de2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="89de2-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89de2-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="89de2-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="89de2-145">Namespace</span></span><br/>                | <span data-ttu-id="89de2-146">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="89de2-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="89de2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="89de2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89de2-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="89de2-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89de2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="89de2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89de2-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89de2-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89de2-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89de2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89de2-152">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="89de2-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

