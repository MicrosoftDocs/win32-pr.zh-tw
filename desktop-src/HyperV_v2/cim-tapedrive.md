---
description: 代表磁帶機的功能和管理。
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: 'CIM_TapeDrive 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981524"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="32653-103">CIM_TapeDrive 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="32653-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="32653-104">代表磁帶機的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="32653-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="32653-105">語法</span><span class="sxs-lookup"><span data-stu-id="32653-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="32653-106">成員</span><span class="sxs-lookup"><span data-stu-id="32653-106">Members</span></span>

<span data-ttu-id="32653-107">**CIM \_ disable-tapedrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32653-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="32653-108">屬性</span><span class="sxs-lookup"><span data-stu-id="32653-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32653-109">屬性</span><span class="sxs-lookup"><span data-stu-id="32653-109">Properties</span></span>

<span data-ttu-id="32653-110">**CIM \_ disable-tapedrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="32653-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32653-111">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="32653-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32653-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="32653-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32653-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32653-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32653-114">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="32653-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="32653-115">指定為「磁帶結尾」之區域的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="32653-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="32653-116">此區域中的存取會產生「磁帶結束」警告。</span><span class="sxs-lookup"><span data-stu-id="32653-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="32653-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="32653-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32653-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="32653-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32653-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32653-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32653-120">磁帶機的最大分割區計數。</span><span class="sxs-lookup"><span data-stu-id="32653-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="32653-121">**MaxRewindTime**</span><span class="sxs-lookup"><span data-stu-id="32653-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32653-122">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="32653-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32653-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32653-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32653-124">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) </span><span class="sxs-lookup"><span data-stu-id="32653-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="32653-125">以毫秒為單位的時間，從磁帶上的最遠距離點移到一開始。</span><span class="sxs-lookup"><span data-stu-id="32653-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="32653-126">**填補**</span><span class="sxs-lookup"><span data-stu-id="32653-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32653-127">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="32653-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32653-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32653-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32653-129">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="32653-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="32653-130">在磁帶媒體上的區塊之間插入的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="32653-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32653-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="32653-131">Requirements</span></span>



| <span data-ttu-id="32653-132">需求</span><span class="sxs-lookup"><span data-stu-id="32653-132">Requirement</span></span> | <span data-ttu-id="32653-133">值</span><span class="sxs-lookup"><span data-stu-id="32653-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32653-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32653-134">Minimum supported client</span></span><br/> | <span data-ttu-id="32653-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="32653-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="32653-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32653-136">Minimum supported server</span></span><br/> | <span data-ttu-id="32653-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="32653-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="32653-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="32653-138">Namespace</span></span><br/>                | <span data-ttu-id="32653-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="32653-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="32653-140">MOF</span><span class="sxs-lookup"><span data-stu-id="32653-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32653-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="32653-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32653-142">DLL</span><span class="sxs-lookup"><span data-stu-id="32653-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32653-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32653-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32653-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32653-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32653-145">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="32653-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

