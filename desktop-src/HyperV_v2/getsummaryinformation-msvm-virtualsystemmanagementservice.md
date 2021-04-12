---
description: 傳回虛擬機器摘要資訊。
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Msvm_VirtualSystemManagementService 類別的 GetSummaryInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318096"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a7a8d-103">Msvm VirtualSystemManagementService 類別的 GetSummaryInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a7a8d-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a7a8d-104">傳回虛擬機器摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a8d-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7a8d-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="a7a8d-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7a8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7a8d-107">*SettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7a8d-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7a8d-108">類型： **CIM \_ VirtualSystemSettingData \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a7a8d-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="a7a8d-109">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))實例的陣列，可指定要抓取資訊的虛擬機器或快照集。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="a7a8d-110">如果此參數為 **Null**，則會取出所有虛擬機器的資訊。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a7a8d-111">*RequestedInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7a8d-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7a8d-112">類型： **uint32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a7a8d-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="a7a8d-113">列舉值的陣列，這些值會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 類別中的屬性，以指定要針對在 *SettingData* 陣列中指定的虛擬機器和快照集取得的資料。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="a7a8d-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名稱** (0) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-115">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="a7a8d-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**元素名稱** (1) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-117">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="a7a8d-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**建立時間** (2) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-119">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **CreationTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="a7a8d-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**附注** (3) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-121">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **Notes** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="a7a8d-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**處理器數目** (4) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-123">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **NumberOfProcessors** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="a7a8d-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**小型縮圖影像 (80x60)** (5) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-125">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ThumbnailImage** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="a7a8d-126">將會取出維度為 80 60 的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="a7a8d-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**中縮圖影像 (160x120)** (6) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-128">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ThumbnailImage** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="a7a8d-129">將會取出維度為 160 120 的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="a7a8d-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**大型縮圖影像 (320x240)** (7) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-131">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ThumbnailImage** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="a7a8d-132">將會取出維度為 320 240 的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="a7a8d-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-134">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **AllocatedGPU** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="a7a8d-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="a7a8d-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**版本** (10) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a7a8d-137">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="a7a8d-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**受防護** 的 (11) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a7a8d-139">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="a7a8d-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-141">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="a7a8d-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-143">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ProcessorLoad** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="a7a8d-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-145">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ProcessorLoadHistory** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="a7a8d-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-147">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **MemoryUsage** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="a7a8d-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**心跳** (104) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-149">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 [**心跳**] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="a7a8d-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**執行時間** (105) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-151">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **執行時間** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="a7a8d-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-153">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **GuestOperatingSystem** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="a7a8d-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span> (107) 的 **快照** 集</span><span class="sxs-lookup"><span data-stu-id="a7a8d-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-155">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **快照** 集屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="a7a8d-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-157">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **AsynchronousTasks** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="a7a8d-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-159">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **HealthState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="a7a8d-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-161">這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **OperationalStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="a7a8d-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-163">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **StatusDescriptions** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="a7a8d-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-165">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **MemoryAvailable** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="a7a8d-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-167">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **AvailableMemoryBuffer** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="a7a8d-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>複寫 **模式** (114) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-169">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ReplicationMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="a7a8d-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>複寫 **狀態** (115) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-171">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ReplicationState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="a7a8d-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-173">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ReplicationHealth** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="a7a8d-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**應用程式健全狀況** (117) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="a7a8d-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-176">這會對應至 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="a7a8d-177">這是跨主要和延伸關聯性的所有複寫狀態值的陣列。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="a7a8d-178">0索引值一律適用于主要關聯性，如果已啟用延伸複寫，則會在索引1中傳回。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="a7a8d-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-180">這會對應至 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationHealth** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="a7a8d-181">這是跨主要和延伸關聯性的所有複寫健全狀況值的陣列。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="a7a8d-182">0索引值一律適用于主要關聯性，如果已啟用延伸複寫，則會在索引1中傳回。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="a7a8d-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-184">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **SwapFilesInUse** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="a7a8d-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="a7a8d-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-187">這會對應到 [**Msvm \_ ReplicationProvider**](msvm-replicationprovider.md)類別的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="a7a8d-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="a7a8d-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-190">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **IntegrationServicesVersionState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="a7a8d-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="a7a8d-192">這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **OtherEnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="a7a8d-193"> (133) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a7a8d-194">*SummaryInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a7a8d-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7a8d-195">類型： **[ **Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="a7a8d-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="a7a8d-196">[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)實例的陣列，其中包含在 *SettingData* 陣列中指定的虛擬機器和/或快照集所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="a7a8d-197">此陣列的元素數會與 *SettingData* 陣列相同。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="a7a8d-198">這些專案中的每一個都會包含 **Name** 屬性，即使沒有要求這個屬性也是一樣。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="a7a8d-199">如果找不到虛擬機器或快照集，或無法使用，則對應摘要資訊專案的 [ **名稱** ] 屬性會是空的。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="a7a8d-200">未在 *RequestedInformation* 參數中指定的屬性會有 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="a7a8d-201">從 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)的1703版 Windows 10 中更新的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7a8d-202">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7a8d-202">Return value</span></span>

<span data-ttu-id="a7a8d-203">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7a8d-203">Type: **uint32**</span></span>

<span data-ttu-id="a7a8d-204">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a7a8d-205">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-206">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-207">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-208">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-209">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-210">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-211">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-212">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-213">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-214">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-215">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-216">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a7a8d-217">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="a7a8d-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a7a8d-218">備註</span><span class="sxs-lookup"><span data-stu-id="a7a8d-218">Remarks</span></span>

<span data-ttu-id="a7a8d-219">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a7a8d-220">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a7a8d-221">範例</span><span class="sxs-lookup"><span data-stu-id="a7a8d-221">Examples</span></span>

<span data-ttu-id="a7a8d-222">下列 c # 範例會顯示摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="a7a8d-223">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7a8d-224">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="a7a8d-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="a7a8d-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7a8d-225">Requirements</span></span>



| <span data-ttu-id="a7a8d-226">需求</span><span class="sxs-lookup"><span data-stu-id="a7a8d-226">Requirement</span></span> | <span data-ttu-id="a7a8d-227">值</span><span class="sxs-lookup"><span data-stu-id="a7a8d-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a8d-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7a8d-228">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a8d-229">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7a8d-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a7a8d-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7a8d-230">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a8d-231">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7a8d-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7a8d-232">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7a8d-232">Namespace</span></span><br/>                | <span data-ttu-id="a7a8d-233">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a7a8d-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a7a8d-234">MOF</span><span class="sxs-lookup"><span data-stu-id="a7a8d-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7a8d-235"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a7a8d-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7a8d-236">DLL</span><span class="sxs-lookup"><span data-stu-id="a7a8d-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7a8d-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7a8d-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a7a8d-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7a8d-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a8d-239">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a7a8d-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="a7a8d-240">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7a8d-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a7a8d-241">**Msvm \_ SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="a7a8d-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

