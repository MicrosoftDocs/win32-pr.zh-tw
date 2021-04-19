---
description: 代表管理 SCSI 介面的通訊協定控制器。
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: CIM_SCSIProtocolController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966739"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="520ce-103">CIM \_ SCSIProtocolController 類別</span><span class="sxs-lookup"><span data-stu-id="520ce-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="520ce-104">代表管理 SCSI 介面的通訊協定控制器。</span><span class="sxs-lookup"><span data-stu-id="520ce-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="520ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="520ce-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="520ce-106">成員</span><span class="sxs-lookup"><span data-stu-id="520ce-106">Members</span></span>

<span data-ttu-id="520ce-107">**CIM \_ SCSIProtocolController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="520ce-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="520ce-108">屬性</span><span class="sxs-lookup"><span data-stu-id="520ce-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="520ce-109">屬性</span><span class="sxs-lookup"><span data-stu-id="520ce-109">Properties</span></span>

<span data-ttu-id="520ce-110">**CIM \_ SCSIProtocolController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="520ce-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="520ce-111">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="520ce-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="520ce-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="520ce-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="520ce-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="520ce-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="520ce-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SCSIProtocolController**.**Name**"，"**CIM \_ SCSIProtocolController**。**OtherNameFormat**") </span><span class="sxs-lookup"><span data-stu-id="520ce-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="520ce-115">**CIM \_ SCSIProtocolController** 的 **名稱** 屬性格式。</span><span class="sxs-lookup"><span data-stu-id="520ce-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="520ce-116">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="520ce-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="520ce-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="520ce-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="520ce-118">**FC 埠 WWN** (2) </span><span class="sxs-lookup"><span data-stu-id="520ce-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="520ce-119">**ISCSI 名稱** (3) </span><span class="sxs-lookup"><span data-stu-id="520ce-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="520ce-120">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="520ce-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="520ce-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="520ce-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="520ce-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="520ce-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="520ce-123">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SCSIProtocolController**.**Name**"，"**CIM \_ SCSIProtocolController**。**NameFormat**") </span><span class="sxs-lookup"><span data-stu-id="520ce-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="520ce-124">當 **NameFormat** 設為 "1" (其他) 時， **NameFormat** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="520ce-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="520ce-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="520ce-125">Requirements</span></span>



| <span data-ttu-id="520ce-126">需求</span><span class="sxs-lookup"><span data-stu-id="520ce-126">Requirement</span></span> | <span data-ttu-id="520ce-127">值</span><span class="sxs-lookup"><span data-stu-id="520ce-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520ce-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="520ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="520ce-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="520ce-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="520ce-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="520ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="520ce-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="520ce-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="520ce-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="520ce-132">Namespace</span></span><br/>                | <span data-ttu-id="520ce-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="520ce-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="520ce-134">MOF</span><span class="sxs-lookup"><span data-stu-id="520ce-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="520ce-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="520ce-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="520ce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="520ce-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="520ce-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="520ce-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="520ce-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="520ce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520ce-139">**CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="520ce-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

