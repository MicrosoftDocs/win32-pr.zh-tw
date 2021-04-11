---
description: 表示由檔案系統透過磁片 DeviceID (key) 欄位識別的連續邏輯區塊範圍。
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: 'CIM_LogicalDisk 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944773"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="65531-103">CIM_LogicalDisk 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="65531-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="65531-104">表示由檔案系統透過磁片 **DeviceID** (key) 欄位識別的連續邏輯區塊範圍。</span><span class="sxs-lookup"><span data-stu-id="65531-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="65531-105">例如，在 Windows 環境中， **DeviceID** 欄位包含磁碟機號;在 UNIX 環境中，它包含存取路徑;在 NetWare 環境中，它包含磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="65531-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="65531-106">語法</span><span class="sxs-lookup"><span data-stu-id="65531-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="65531-107">成員</span><span class="sxs-lookup"><span data-stu-id="65531-107">Members</span></span>

<span data-ttu-id="65531-108">**CIM \_ LogicalDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65531-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="65531-109">屬性</span><span class="sxs-lookup"><span data-stu-id="65531-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65531-110">屬性</span><span class="sxs-lookup"><span data-stu-id="65531-110">Properties</span></span>

<span data-ttu-id="65531-111">**CIM \_ LogicalDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="65531-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65531-112">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="65531-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65531-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="65531-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65531-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65531-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65531-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NameFormat" ) </span><span class="sxs-lookup"><span data-stu-id="65531-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="65531-116">指出邏輯裝置是否使用 OS 的名稱格式。</span><span class="sxs-lookup"><span data-stu-id="65531-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="65531-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="65531-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="65531-118">**OS 裝置名稱** (12) </span><span class="sxs-lookup"><span data-stu-id="65531-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="65531-119">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="65531-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65531-120">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="65531-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65531-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65531-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65531-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NameNamespace" ) </span><span class="sxs-lookup"><span data-stu-id="65531-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="65531-123">指出邏輯裝置是否與作業系統具有相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="65531-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="65531-124">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="65531-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="65531-125">**OS 裝置命名空間** (8) </span><span class="sxs-lookup"><span data-stu-id="65531-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="65531-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="65531-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="65531-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="65531-127">Requirements</span></span>



| <span data-ttu-id="65531-128">需求</span><span class="sxs-lookup"><span data-stu-id="65531-128">Requirement</span></span> | <span data-ttu-id="65531-129">值</span><span class="sxs-lookup"><span data-stu-id="65531-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65531-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65531-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65531-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="65531-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="65531-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65531-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65531-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65531-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="65531-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="65531-134">Namespace</span></span><br/>                | <span data-ttu-id="65531-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="65531-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="65531-136">MOF</span><span class="sxs-lookup"><span data-stu-id="65531-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65531-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="65531-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65531-138">DLL</span><span class="sxs-lookup"><span data-stu-id="65531-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65531-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65531-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="65531-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65531-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65531-141">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="65531-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

