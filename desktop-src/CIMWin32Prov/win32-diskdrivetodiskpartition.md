---
description: Win32 \_ DiskDriveToDiskPartition 關聯 WMI 類別會關聯磁片磁碟機和其上現有的磁碟分割。
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971142"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="2cb59-103">Win32 \_ DiskDriveToDiskPartition 類別</span><span class="sxs-lookup"><span data-stu-id="2cb59-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="2cb59-104">**Win32 \_ DiskDriveToDiskPartition** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯磁片磁碟機和其上現有的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="2cb59-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="2cb59-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb59-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2cb59-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2cb59-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb59-107">語法</span><span class="sxs-lookup"><span data-stu-id="2cb59-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2cb59-108">成員</span><span class="sxs-lookup"><span data-stu-id="2cb59-108">Members</span></span>

<span data-ttu-id="2cb59-109">**Win32 \_ DiskDriveToDiskPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2cb59-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="2cb59-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2cb59-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cb59-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2cb59-111">Properties</span></span>

<span data-ttu-id="2cb59-112">**Win32 \_ DiskDriveToDiskPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb59-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cb59-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="2cb59-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb59-114">資料類型： **Win32 \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="2cb59-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="2cb59-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2cb59-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb59-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DiskDrive" ) </span><span class="sxs-lookup"><span data-stu-id="2cb59-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="2cb59-117">此實例的參考，代表磁碟分割所在之磁片磁碟機的屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb59-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="2cb59-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="2cb59-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb59-119">資料類型： **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="2cb59-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="2cb59-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2cb59-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb59-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 DiskPartition」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="2cb59-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="2cb59-122">代表位於磁片磁碟機上的磁碟分割之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="2cb59-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cb59-123">備註</span><span class="sxs-lookup"><span data-stu-id="2cb59-123">Remarks</span></span>

<span data-ttu-id="2cb59-124">**Win32 \_ DiskDriveToDiskPartition** 類別衍生自 [**CIM \_ MediaPresent**](cim-mediapresent.md)。</span><span class="sxs-lookup"><span data-stu-id="2cb59-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="2cb59-125">如需如何使用這個類別的討論，請參閱 [使用 PowerShell 對應磁片磁碟機和磁碟分割](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) ，以及 [如何將邏輯磁碟機和實體磁片相互關聯？](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog 文章。</span><span class="sxs-lookup"><span data-stu-id="2cb59-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="2cb59-126">範例</span><span class="sxs-lookup"><span data-stu-id="2cb59-126">Examples</span></span>

<span data-ttu-id="2cb59-127">[使用 Powershell 收集磁片/磁碟分割/掛接點資訊](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0)powershell 範例會使用 **Win32 \_ DiskDriveToDiskPartition** 來傳回本機磁片/磁碟分割和掛接點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2cb59-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb59-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cb59-128">Requirements</span></span>



| <span data-ttu-id="2cb59-129">需求</span><span class="sxs-lookup"><span data-stu-id="2cb59-129">Requirement</span></span> | <span data-ttu-id="2cb59-130">值</span><span class="sxs-lookup"><span data-stu-id="2cb59-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb59-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2cb59-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb59-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cb59-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2cb59-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2cb59-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb59-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cb59-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2cb59-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="2cb59-135">Namespace</span></span><br/>                | <span data-ttu-id="2cb59-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2cb59-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2cb59-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2cb59-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cb59-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cb59-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cb59-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb59-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb59-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb59-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb59-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cb59-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb59-142">**CIM \_ MediaPresent**</span><span class="sxs-lookup"><span data-stu-id="2cb59-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="2cb59-143">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2cb59-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2cb59-144">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="2cb59-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

