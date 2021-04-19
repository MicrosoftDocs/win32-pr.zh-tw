---
description: 表示將轉寄資料庫的專案套用至交換器埠的關聯。
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: CIM_SwitchPortDynamicForwarding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988741"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="85d57-103">CIM \_ SwitchPortDynamicForwarding 類別</span><span class="sxs-lookup"><span data-stu-id="85d57-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="85d57-104">表示將轉寄資料庫的專案套用至交換器埠的關聯。</span><span class="sxs-lookup"><span data-stu-id="85d57-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d57-105">語法</span><span class="sxs-lookup"><span data-stu-id="85d57-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="85d57-106">成員</span><span class="sxs-lookup"><span data-stu-id="85d57-106">Members</span></span>

<span data-ttu-id="85d57-107">**CIM \_ SwitchPortDynamicForwarding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="85d57-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="85d57-108">屬性</span><span class="sxs-lookup"><span data-stu-id="85d57-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85d57-109">屬性</span><span class="sxs-lookup"><span data-stu-id="85d57-109">Properties</span></span>

<span data-ttu-id="85d57-110">**CIM \_ SwitchPortDynamicForwarding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="85d57-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85d57-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="85d57-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d57-112">資料類型： **CIM 執行 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="85d57-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="85d57-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85d57-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85d57-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) ， [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="85d57-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="85d57-115">交換器埠的 CIM 同參數參考。 [**\_**](cim-switchport.md)</span><span class="sxs-lookup"><span data-stu-id="85d57-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="85d57-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="85d57-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d57-117">資料類型： **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="85d57-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="85d57-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85d57-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85d57-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="85d57-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="85d57-120">轉送資料庫專案的 [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="85d57-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85d57-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="85d57-121">Requirements</span></span>



| <span data-ttu-id="85d57-122">需求</span><span class="sxs-lookup"><span data-stu-id="85d57-122">Requirement</span></span> | <span data-ttu-id="85d57-123">值</span><span class="sxs-lookup"><span data-stu-id="85d57-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85d57-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85d57-124">Minimum supported client</span></span><br/> | <span data-ttu-id="85d57-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="85d57-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="85d57-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85d57-126">Minimum supported server</span></span><br/> | <span data-ttu-id="85d57-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85d57-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="85d57-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="85d57-128">Namespace</span></span><br/>                | <span data-ttu-id="85d57-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="85d57-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="85d57-130">MOF</span><span class="sxs-lookup"><span data-stu-id="85d57-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85d57-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="85d57-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85d57-132">DLL</span><span class="sxs-lookup"><span data-stu-id="85d57-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85d57-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85d57-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85d57-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85d57-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d57-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="85d57-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

