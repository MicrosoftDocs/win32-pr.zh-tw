---
description: 表示埠 RDMA 功能設定資料。
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Msvm_EthernetSwitchPortRdmaSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853156"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="39dba-103">Msvm \_ EthernetSwitchPortRdmaSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="39dba-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="39dba-104">表示埠 RDMA 功能設定資料。</span><span class="sxs-lookup"><span data-stu-id="39dba-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="39dba-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="39dba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39dba-106">語法</span><span class="sxs-lookup"><span data-stu-id="39dba-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="39dba-107">成員</span><span class="sxs-lookup"><span data-stu-id="39dba-107">Members</span></span>

<span data-ttu-id="39dba-108">**Msvm \_ EthernetSwitchPortRdmaSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="39dba-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="39dba-109">屬性</span><span class="sxs-lookup"><span data-stu-id="39dba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39dba-110">屬性</span><span class="sxs-lookup"><span data-stu-id="39dba-110">Properties</span></span>

<span data-ttu-id="39dba-111">**Msvm \_ EthernetSwitchPortRdmaSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="39dba-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39dba-112">**RdmaOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="39dba-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dba-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39dba-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39dba-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="39dba-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="39dba-115">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="39dba-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="39dba-116">針對來賓 RDMA 指派給此埠的加權。</span><span class="sxs-lookup"><span data-stu-id="39dba-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="39dba-117">加權是指派 RDMA 資源時的相對重要性。</span><span class="sxs-lookup"><span data-stu-id="39dba-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="39dba-118">將 **RdmaOffloadWeight** 屬性設定為0會停用埠上的 RDMA。</span><span class="sxs-lookup"><span data-stu-id="39dba-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="39dba-119">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="39dba-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39dba-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="39dba-120">Requirements</span></span>



| <span data-ttu-id="39dba-121">需求</span><span class="sxs-lookup"><span data-stu-id="39dba-121">Requirement</span></span> | <span data-ttu-id="39dba-122">值</span><span class="sxs-lookup"><span data-stu-id="39dba-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39dba-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39dba-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39dba-124">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39dba-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39dba-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39dba-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39dba-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="39dba-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="39dba-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="39dba-127">Namespace</span></span><br/>                | <span data-ttu-id="39dba-128">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="39dba-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="39dba-129">MOF</span><span class="sxs-lookup"><span data-stu-id="39dba-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39dba-130"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="39dba-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39dba-131">DLL</span><span class="sxs-lookup"><span data-stu-id="39dba-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39dba-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39dba-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39dba-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39dba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39dba-134">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="39dba-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




