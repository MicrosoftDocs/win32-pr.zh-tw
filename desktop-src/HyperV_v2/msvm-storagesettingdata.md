---
description: 表示虛擬系統的儲存特定設定。
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998909"
---
# <a name="msvm_storagesettingdata-class"></a><span data-ttu-id="f10ea-103">Msvm \_ StorageSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="f10ea-103">Msvm\_StorageSettingData class</span></span>

<span data-ttu-id="f10ea-104">表示虛擬系統的儲存特定設定。</span><span class="sxs-lookup"><span data-stu-id="f10ea-104">Represents the storage-specific settings for a virtual system.</span></span>

<span data-ttu-id="f10ea-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f10ea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="f10ea-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a><span data-ttu-id="f10ea-107">成員</span><span class="sxs-lookup"><span data-stu-id="f10ea-107">Members</span></span>

<span data-ttu-id="f10ea-108">**Msvm \_ StorageSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f10ea-108">The **Msvm\_StorageSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f10ea-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f10ea-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f10ea-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f10ea-110">Properties</span></span>

<span data-ttu-id="f10ea-111">**Msvm \_ StorageSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f10ea-111">The **Msvm\_StorageSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f10ea-112">**DisableInterruptBatching**</span><span class="sxs-lookup"><span data-stu-id="f10ea-112">**DisableInterruptBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f10ea-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f10ea-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f10ea-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f10ea-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f10ea-115">指定是否應該停用中斷批次處理。</span><span class="sxs-lookup"><span data-stu-id="f10ea-115">Specifies whether interrupt batching should be disabled.</span></span>

<span data-ttu-id="f10ea-116">這是唯讀屬性，但是可以使用 Wmi [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="f10ea-116">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the Wmi [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f10ea-117">**ThreadCountPerChannel**</span><span class="sxs-lookup"><span data-stu-id="f10ea-117">**ThreadCountPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f10ea-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f10ea-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f10ea-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f10ea-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f10ea-120">處理 IO 的每個儲存通道執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="f10ea-120">The number of threads per storage channel to process IO.</span></span>

<span data-ttu-id="f10ea-121">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="f10ea-121">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="f10ea-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**預設** (0) </span><span class="sxs-lookup"><span data-stu-id="f10ea-122"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f10ea-123">預設行為</span><span class="sxs-lookup"><span data-stu-id="f10ea-123">Default behavior</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="f10ea-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (1) </span><span class="sxs-lookup"><span data-stu-id="f10ea-124"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f10ea-125">每個儲存體通道的執行緒數目下限。</span><span class="sxs-lookup"><span data-stu-id="f10ea-125">Low number of threads per storage channel.</span></span>

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="f10ea-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**中型** (2) </span><span class="sxs-lookup"><span data-stu-id="f10ea-126"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f10ea-127">每個儲存體通道的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="f10ea-127">Medium number of threads per storage channel.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="f10ea-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (3) </span><span class="sxs-lookup"><span data-stu-id="f10ea-128"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f10ea-129">每個儲存體通道有大量的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f10ea-129">High number of threads per storage channel.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f10ea-130">**VirtualProcessorsPerChannel**</span><span class="sxs-lookup"><span data-stu-id="f10ea-130">**VirtualProcessorsPerChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f10ea-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f10ea-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f10ea-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f10ea-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f10ea-133">每個儲存體通道的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="f10ea-133">The number of processors per storage channel.</span></span> <span data-ttu-id="f10ea-134">要開啟的通道數目是由主機/**VirtualProcessorsPerChannel**) 上的 (邏輯處理器計數所指定。</span><span class="sxs-lookup"><span data-stu-id="f10ea-134">The number of channels to be opened is given by (Count of logical processors on the host /**VirtualProcessorsPerChannel**).</span></span>

<span data-ttu-id="f10ea-135">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="f10ea-135">This is a read-only property, but it can be changed using the [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f10ea-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="f10ea-136">Requirements</span></span>



| <span data-ttu-id="f10ea-137">需求</span><span class="sxs-lookup"><span data-stu-id="f10ea-137">Requirement</span></span> | <span data-ttu-id="f10ea-138">值</span><span class="sxs-lookup"><span data-stu-id="f10ea-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f10ea-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f10ea-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f10ea-140">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f10ea-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f10ea-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f10ea-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f10ea-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f10ea-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f10ea-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="f10ea-143">Namespace</span></span><br/>                | <span data-ttu-id="f10ea-144">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f10ea-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f10ea-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f10ea-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f10ea-146"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f10ea-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f10ea-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f10ea-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f10ea-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f10ea-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f10ea-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f10ea-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f10ea-150">**Msvm \_ SystemComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="f10ea-150">**Msvm\_SystemComponentSettingData**</span></span>](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




