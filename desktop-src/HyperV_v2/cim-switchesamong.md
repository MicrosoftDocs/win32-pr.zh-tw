---
description: 代表切換服務，此服務會在交換器埠之間切換框架。
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: CIM_SwitchesAmong 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113573"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="16b2f-103">CIM \_ SwitchesAmong 類別</span><span class="sxs-lookup"><span data-stu-id="16b2f-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="16b2f-104">代表切換服務，此服務會在交換器埠之間切換框架。</span><span class="sxs-lookup"><span data-stu-id="16b2f-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="16b2f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="16b2f-106">成員</span><span class="sxs-lookup"><span data-stu-id="16b2f-106">Members</span></span>

<span data-ttu-id="16b2f-107">**CIM \_ SwitchesAmong** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16b2f-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="16b2f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="16b2f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16b2f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="16b2f-109">Properties</span></span>

<span data-ttu-id="16b2f-110">**CIM \_ SwitchesAmong** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16b2f-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16b2f-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="16b2f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b2f-112">資料類型： **CIM 執行 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="16b2f-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="16b2f-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b2f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16b2f-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="16b2f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="16b2f-115">交換器埠的 CIM 同參數參考。 [**\_**](cim-switchport.md)</span><span class="sxs-lookup"><span data-stu-id="16b2f-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="16b2f-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="16b2f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b2f-117">資料類型： **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="16b2f-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="16b2f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b2f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16b2f-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="16b2f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="16b2f-120">切換服務的 [**CIM \_ SwitchService**](cim-switchservice.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="16b2f-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16b2f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b2f-121">Requirements</span></span>



| <span data-ttu-id="16b2f-122">需求</span><span class="sxs-lookup"><span data-stu-id="16b2f-122">Requirement</span></span> | <span data-ttu-id="16b2f-123">值</span><span class="sxs-lookup"><span data-stu-id="16b2f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b2f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16b2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="16b2f-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16b2f-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="16b2f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16b2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="16b2f-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16b2f-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="16b2f-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="16b2f-128">Namespace</span></span><br/>                | <span data-ttu-id="16b2f-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="16b2f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16b2f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="16b2f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16b2f-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="16b2f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16b2f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="16b2f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b2f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16b2f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16b2f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16b2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b2f-135">**CIM \_ ForwardsAmong**</span><span class="sxs-lookup"><span data-stu-id="16b2f-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 

