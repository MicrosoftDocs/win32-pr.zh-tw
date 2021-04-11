---
description: 將序列埠與序列控制器產生關聯。
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848257"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="a9386-103">Msvm \_ SerialPortOnSerialController 類別</span><span class="sxs-lookup"><span data-stu-id="a9386-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="a9386-104">將序列埠與序列控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a9386-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="a9386-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9386-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9386-106">語法</span><span class="sxs-lookup"><span data-stu-id="a9386-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a9386-107">成員</span><span class="sxs-lookup"><span data-stu-id="a9386-107">Members</span></span>

<span data-ttu-id="a9386-108">**Msvm \_ SerialPortOnSerialController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9386-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="a9386-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a9386-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9386-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a9386-110">Properties</span></span>

<span data-ttu-id="a9386-111">**Msvm \_ SerialPortOnSerialController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a9386-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9386-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="a9386-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9386-113">資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="a9386-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="a9386-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9386-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9386-115">埠所連接的序列控制器。</span><span class="sxs-lookup"><span data-stu-id="a9386-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="a9386-116">這個屬性繼承自 [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)。</span><span class="sxs-lookup"><span data-stu-id="a9386-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="a9386-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="a9386-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9386-118">資料類型： **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a9386-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="a9386-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9386-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9386-120">序列控制器的通訊埠。</span><span class="sxs-lookup"><span data-stu-id="a9386-120">The port of the serial controller.</span></span> <span data-ttu-id="a9386-121">這個屬性繼承自 [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)。</span><span class="sxs-lookup"><span data-stu-id="a9386-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9386-122">備註</span><span class="sxs-lookup"><span data-stu-id="a9386-122">Remarks</span></span>

<span data-ttu-id="a9386-123">存取 **Msvm \_ SerialPortOnSerialController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a9386-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a9386-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a9386-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9386-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9386-125">Requirements</span></span>



| <span data-ttu-id="a9386-126">需求</span><span class="sxs-lookup"><span data-stu-id="a9386-126">Requirement</span></span> | <span data-ttu-id="a9386-127">值</span><span class="sxs-lookup"><span data-stu-id="a9386-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9386-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9386-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a9386-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9386-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a9386-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9386-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a9386-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9386-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9386-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="a9386-132">Namespace</span></span><br/>                | <span data-ttu-id="a9386-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a9386-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9386-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a9386-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9386-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a9386-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9386-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a9386-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9386-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9386-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9386-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9386-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9386-139">**CIM \_ PortOnDevice**</span><span class="sxs-lookup"><span data-stu-id="a9386-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="a9386-140">**CIM \_ PortOnDevice**</span><span class="sxs-lookup"><span data-stu-id="a9386-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="a9386-141">序列裝置類別</span><span class="sxs-lookup"><span data-stu-id="a9386-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

