---
description: 表示 PCI Express 埠的狀態。
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Msvm_PciExpress 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987794"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="94314-103">Msvm \_ PciExpress 類別</span><span class="sxs-lookup"><span data-stu-id="94314-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="94314-104">表示 PCI Express 埠的狀態。</span><span class="sxs-lookup"><span data-stu-id="94314-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="94314-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="94314-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94314-106">語法</span><span class="sxs-lookup"><span data-stu-id="94314-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="94314-107">成員</span><span class="sxs-lookup"><span data-stu-id="94314-107">Members</span></span>

<span data-ttu-id="94314-108">**Msvm \_ PciExpress** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="94314-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="94314-109">屬性</span><span class="sxs-lookup"><span data-stu-id="94314-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94314-110">屬性</span><span class="sxs-lookup"><span data-stu-id="94314-110">Properties</span></span>

<span data-ttu-id="94314-111">**Msvm \_ PciExpress** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="94314-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94314-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="94314-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94314-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94314-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94314-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94314-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94314-115">包含識別裝置虛擬 PCI Express 裝置之裝置實例路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="94314-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="94314-116">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="94314-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94314-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="94314-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94314-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94314-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94314-119">虛擬 PCI Express 裝置的功能編號。</span><span class="sxs-lookup"><span data-stu-id="94314-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="94314-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="94314-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94314-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94314-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94314-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94314-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94314-123">字串，包含識別裝置虛擬 PCI Express 裝置的裝置位置路徑。</span><span class="sxs-lookup"><span data-stu-id="94314-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94314-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="94314-124">Requirements</span></span>



| <span data-ttu-id="94314-125">需求</span><span class="sxs-lookup"><span data-stu-id="94314-125">Requirement</span></span> | <span data-ttu-id="94314-126">值</span><span class="sxs-lookup"><span data-stu-id="94314-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94314-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94314-127">Minimum supported client</span></span><br/> | <span data-ttu-id="94314-128">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94314-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="94314-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94314-129">Minimum supported server</span></span><br/> | <span data-ttu-id="94314-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="94314-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="94314-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="94314-131">Namespace</span></span><br/>                | <span data-ttu-id="94314-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="94314-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="94314-133">MOF</span><span class="sxs-lookup"><span data-stu-id="94314-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94314-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="94314-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94314-135">DLL</span><span class="sxs-lookup"><span data-stu-id="94314-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94314-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94314-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94314-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94314-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94314-138">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="94314-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




