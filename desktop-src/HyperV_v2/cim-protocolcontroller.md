---
description: 代表控制器的群組，這些控制器控制起始通訊協定之裝置的作業和運作。
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: CIM_ProtocolController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27372bc57ad36f37689d75b3963ec0c4b1106956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972805"
---
# <a name="cim_protocolcontroller-class"></a><span data-ttu-id="c7c66-103">CIM \_ ProtocolController 類別</span><span class="sxs-lookup"><span data-stu-id="c7c66-103">CIM\_ProtocolController class</span></span>

<span data-ttu-id="c7c66-104">代表控制器的群組，這些控制器控制起始通訊協定之裝置的作業和運作。</span><span class="sxs-lookup"><span data-stu-id="c7c66-104">Represents a group of controllers that control the operation and function of devices that initiate protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c66-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7c66-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a><span data-ttu-id="c7c66-106">成員</span><span class="sxs-lookup"><span data-stu-id="c7c66-106">Members</span></span>

<span data-ttu-id="c7c66-107">**CIM \_ ProtocolController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7c66-107">The **CIM\_ProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="c7c66-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c7c66-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7c66-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c7c66-109">Properties</span></span>

<span data-ttu-id="c7c66-110">**CIM \_ ProtocolController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c7c66-110">The **CIM\_ProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7c66-111">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="c7c66-111">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c66-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7c66-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7c66-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c66-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c66-114">可透過通訊協定控制器控制或存取的單位數目上限。</span><span class="sxs-lookup"><span data-stu-id="c7c66-114">The maximum number of units that can be controlled by or accessed through the protocol controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7c66-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7c66-115">Requirements</span></span>



| <span data-ttu-id="c7c66-116">需求</span><span class="sxs-lookup"><span data-stu-id="c7c66-116">Requirement</span></span> | <span data-ttu-id="c7c66-117">值</span><span class="sxs-lookup"><span data-stu-id="c7c66-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c66-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7c66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c66-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7c66-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7c66-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7c66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c66-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7c66-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7c66-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7c66-122">Namespace</span></span><br/>                | <span data-ttu-id="c7c66-123">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7c66-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c7c66-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c7c66-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7c66-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c7c66-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7c66-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c66-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c66-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7c66-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7c66-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7c66-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c66-129">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c7c66-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




