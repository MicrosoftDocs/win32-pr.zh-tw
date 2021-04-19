---
description: 將透明橋接服務與轉送資料庫的專案產生關聯。
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: CIM_TransparentBridgingDynamicForwarding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977266"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="8393c-103">CIM \_ TransparentBridgingDynamicForwarding 類別</span><span class="sxs-lookup"><span data-stu-id="8393c-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="8393c-104">將透明橋接服務與轉送資料庫的專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8393c-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8393c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8393c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8393c-106">成員</span><span class="sxs-lookup"><span data-stu-id="8393c-106">Members</span></span>

<span data-ttu-id="8393c-107">**CIM \_ TransparentBridgingDynamicForwarding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8393c-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="8393c-108">屬性</span><span class="sxs-lookup"><span data-stu-id="8393c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8393c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8393c-109">Properties</span></span>

<span data-ttu-id="8393c-110">**CIM \_ TransparentBridgingDynamicForwarding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8393c-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8393c-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="8393c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8393c-112">資料類型： **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="8393c-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="8393c-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8393c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8393c-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="8393c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8393c-115">透明橋接服務的 [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="8393c-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="8393c-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8393c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8393c-117">資料類型： **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="8393c-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="8393c-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8393c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8393c-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="8393c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8393c-120">轉送資料庫專案的 [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="8393c-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8393c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8393c-121">Requirements</span></span>



| <span data-ttu-id="8393c-122">需求</span><span class="sxs-lookup"><span data-stu-id="8393c-122">Requirement</span></span> | <span data-ttu-id="8393c-123">值</span><span class="sxs-lookup"><span data-stu-id="8393c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8393c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8393c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8393c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8393c-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8393c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8393c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8393c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8393c-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8393c-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="8393c-128">Namespace</span></span><br/>                | <span data-ttu-id="8393c-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8393c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8393c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8393c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8393c-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8393c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8393c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8393c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8393c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8393c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8393c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8393c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8393c-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="8393c-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

