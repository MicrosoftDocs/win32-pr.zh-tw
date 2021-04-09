---
description: 服務存取點之間的關聯 (SAP) 與其如何實行。
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847963"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="3bda9-103">Msvm \_ WiFiDeviceSAPImplementation 類別</span><span class="sxs-lookup"><span data-stu-id="3bda9-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="3bda9-104">服務存取點之間的關聯 (SAP) 與其如何實行。</span><span class="sxs-lookup"><span data-stu-id="3bda9-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="3bda9-105">此關聯的基數為多對多。</span><span class="sxs-lookup"><span data-stu-id="3bda9-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="3bda9-106">SAP 可由一個以上的邏輯裝置提供，並結合運作。</span><span class="sxs-lookup"><span data-stu-id="3bda9-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="3bda9-107">任何裝置都可以提供一個以上的 SAP。</span><span class="sxs-lookup"><span data-stu-id="3bda9-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="3bda9-108">當有許多邏輯裝置與單一 SAP 相關聯時，會假設這些專案會一起運作以提供存取點。</span><span class="sxs-lookup"><span data-stu-id="3bda9-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="3bda9-109">如果有不同的 SAP 執行，則每個執行都會導致 SAP 物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="3bda9-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="3bda9-110">這些個別的具現化會與唯一的實作為關聯。</span><span class="sxs-lookup"><span data-stu-id="3bda9-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="3bda9-111">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3bda9-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bda9-112">語法</span><span class="sxs-lookup"><span data-stu-id="3bda9-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3bda9-113">成員</span><span class="sxs-lookup"><span data-stu-id="3bda9-113">Members</span></span>

<span data-ttu-id="3bda9-114">**Msvm \_ WiFiDeviceSAPImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3bda9-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="3bda9-115">屬性</span><span class="sxs-lookup"><span data-stu-id="3bda9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bda9-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3bda9-116">Properties</span></span>

<span data-ttu-id="3bda9-117">**Msvm \_ WiFiDeviceSAPImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3bda9-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bda9-118">**先行**</span><span class="sxs-lookup"><span data-stu-id="3bda9-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bda9-119">資料類型： **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="3bda9-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3bda9-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bda9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bda9-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="3bda9-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3bda9-122">代表邏輯裝置之 [**Msvm \_ WiFiPort**](msvm-wifiport.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3bda9-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="3bda9-123">**依賴**</span><span class="sxs-lookup"><span data-stu-id="3bda9-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bda9-124">資料類型： **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="3bda9-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3bda9-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bda9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bda9-126">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="3bda9-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3bda9-127">[**Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)類別的實例，代表使用邏輯裝置所執行的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="3bda9-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bda9-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bda9-128">Requirements</span></span>



| <span data-ttu-id="3bda9-129">需求</span><span class="sxs-lookup"><span data-stu-id="3bda9-129">Requirement</span></span> | <span data-ttu-id="3bda9-130">值</span><span class="sxs-lookup"><span data-stu-id="3bda9-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bda9-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bda9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3bda9-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bda9-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3bda9-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bda9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3bda9-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bda9-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bda9-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="3bda9-135">Namespace</span></span><br/>                | <span data-ttu-id="3bda9-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3bda9-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3bda9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3bda9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bda9-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3bda9-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bda9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3bda9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bda9-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3bda9-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

