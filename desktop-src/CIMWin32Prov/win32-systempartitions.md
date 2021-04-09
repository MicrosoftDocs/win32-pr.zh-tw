---
description: Win32 \_ SystemPartitions 關聯 WMI 類別會關聯電腦系統和該系統上的磁碟分割。
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Win32_SystemPartitions 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847313"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="ceff6-103">Win32 \_ SystemPartitions 類別</span><span class="sxs-lookup"><span data-stu-id="ceff6-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="ceff6-104">**Win32 \_ SystemPartitions** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會關聯電腦系統和該系統上的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="ceff6-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="ceff6-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ceff6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ceff6-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="ceff6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceff6-107">語法</span><span class="sxs-lookup"><span data-stu-id="ceff6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ceff6-108">成員</span><span class="sxs-lookup"><span data-stu-id="ceff6-108">Members</span></span>

<span data-ttu-id="ceff6-109">**Win32 \_ SystemPartitions** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ceff6-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="ceff6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ceff6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ceff6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ceff6-111">Properties</span></span>

<span data-ttu-id="ceff6-112">**Win32 \_ SystemPartitions** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ceff6-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ceff6-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ceff6-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceff6-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="ceff6-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ceff6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ceff6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceff6-116">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI Win32 \| \_ " ) </span><span class="sxs-lookup"><span data-stu-id="ceff6-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="ceff6-117">此實例的參考，代表磁碟分割所在之電腦系統的屬性。</span><span class="sxs-lookup"><span data-stu-id="ceff6-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="ceff6-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ceff6-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceff6-119">資料類型： **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="ceff6-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="ceff6-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ceff6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceff6-121">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ DiskPartition" ) </span><span class="sxs-lookup"><span data-stu-id="ceff6-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="ceff6-122">代表存在於電腦系統上的磁碟分割屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="ceff6-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ceff6-123">備註</span><span class="sxs-lookup"><span data-stu-id="ceff6-123">Remarks</span></span>

<span data-ttu-id="ceff6-124">**Win32 \_ SystemPartitions** 類別衍生自 [**win32 \_ SystemDevices**](win32-systemdevices.md)。</span><span class="sxs-lookup"><span data-stu-id="ceff6-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ceff6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ceff6-125">Requirements</span></span>



| <span data-ttu-id="ceff6-126">需求</span><span class="sxs-lookup"><span data-stu-id="ceff6-126">Requirement</span></span> | <span data-ttu-id="ceff6-127">值</span><span class="sxs-lookup"><span data-stu-id="ceff6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceff6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ceff6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ceff6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceff6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ceff6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ceff6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ceff6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceff6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ceff6-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="ceff6-132">Namespace</span></span><br/>                | <span data-ttu-id="ceff6-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ceff6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ceff6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ceff6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceff6-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceff6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceff6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ceff6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceff6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceff6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceff6-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ceff6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceff6-139">**Win32 \_ SystemDevices**</span><span class="sxs-lookup"><span data-stu-id="ceff6-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="ceff6-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="ceff6-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
