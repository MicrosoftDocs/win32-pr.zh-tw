---
description: 代表 DVD 光碟機。
ms.assetid: 6127b58d-c70f-47c7-9eeb-6aff819f672e
title: CIM_DVDDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DVDDrive
- CIM_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44c69cfe537257076623e472f4bb1406f8bf7665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966762"
---
# <a name="cim_dvddrive-class"></a><span data-ttu-id="42856-103">CIM \_ DVDDrive 類別</span><span class="sxs-lookup"><span data-stu-id="42856-103">CIM\_DVDDrive class</span></span>

<span data-ttu-id="42856-104">代表 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="42856-104">Represents a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="42856-105">語法</span><span class="sxs-lookup"><span data-stu-id="42856-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_DVDDrive : CIM_MediaAccessDevice
{
  uint16 FormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="42856-106">成員</span><span class="sxs-lookup"><span data-stu-id="42856-106">Members</span></span>

<span data-ttu-id="42856-107">**CIM \_ DVDDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42856-107">The **CIM\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="42856-108">屬性</span><span class="sxs-lookup"><span data-stu-id="42856-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42856-109">屬性</span><span class="sxs-lookup"><span data-stu-id="42856-109">Properties</span></span>

<span data-ttu-id="42856-110">**CIM \_ DVDDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42856-110">The **CIM\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42856-111">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="42856-111">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42856-112">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="42856-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="42856-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42856-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42856-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**媒體媒體**) </span><span class="sxs-lookup"><span data-stu-id="42856-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMedia**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="42856-115">裝置支援的 CD 和 DVD 格式。</span><span class="sxs-lookup"><span data-stu-id="42856-115">The CD and DVD formats that are supported by the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="42856-116">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="42856-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="42856-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="42856-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="42856-118">**Cd-rom** (16) </span><span class="sxs-lookup"><span data-stu-id="42856-118">**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="42856-119">**Cd-rom/XA** (17) </span><span class="sxs-lookup"><span data-stu-id="42856-119">**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="42856-120">**CD-I** (18) </span><span class="sxs-lookup"><span data-stu-id="42856-120">**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="42856-121">**CD 可燒錄** (19) </span><span class="sxs-lookup"><span data-stu-id="42856-121">**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="42856-122">**DVD** (22) </span><span class="sxs-lookup"><span data-stu-id="42856-122">**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>

<span data-ttu-id="42856-123">**Dvd-rom +** (23) </span><span class="sxs-lookup"><span data-stu-id="42856-123">**DVD-RW+** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="42856-124">**DVD-RAM** (24) </span><span class="sxs-lookup"><span data-stu-id="42856-124">**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="42856-125">**Dvd-rom** (25) </span><span class="sxs-lookup"><span data-stu-id="42856-125">**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="42856-126">**DVD-影片** (26) </span><span class="sxs-lookup"><span data-stu-id="42856-126">**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="42856-127">**Divx** (27) </span><span class="sxs-lookup"><span data-stu-id="42856-127">**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="42856-128">**Cd-rw (33**) </span><span class="sxs-lookup"><span data-stu-id="42856-128">**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="42856-129">**CD-DA** (34) </span><span class="sxs-lookup"><span data-stu-id="42856-129">**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="42856-130">**CD +** (35) </span><span class="sxs-lookup"><span data-stu-id="42856-130">**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="42856-131">**DVD 可燒錄** (36) </span><span class="sxs-lookup"><span data-stu-id="42856-131">**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="42856-132">**Cd-rw** (37) </span><span class="sxs-lookup"><span data-stu-id="42856-132">**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="42856-133">**DVD-音訊** (38) </span><span class="sxs-lookup"><span data-stu-id="42856-133">**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="42856-134">**DVD-5** (39) </span><span class="sxs-lookup"><span data-stu-id="42856-134">**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="42856-135">**DVD-9** (40) </span><span class="sxs-lookup"><span data-stu-id="42856-135">**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="42856-136">**DVD-10** (41) </span><span class="sxs-lookup"><span data-stu-id="42856-136">**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="42856-137">**DVD-18** (42) </span><span class="sxs-lookup"><span data-stu-id="42856-137">**DVD-18** (42)</span></span>


<span data-ttu-id="42856-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="42856-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="42856-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="42856-139">Requirements</span></span>



| <span data-ttu-id="42856-140">需求</span><span class="sxs-lookup"><span data-stu-id="42856-140">Requirement</span></span> | <span data-ttu-id="42856-141">值</span><span class="sxs-lookup"><span data-stu-id="42856-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42856-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42856-142">Minimum supported client</span></span><br/> | <span data-ttu-id="42856-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="42856-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="42856-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42856-144">Minimum supported server</span></span><br/> | <span data-ttu-id="42856-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42856-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="42856-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="42856-146">Namespace</span></span><br/>                | <span data-ttu-id="42856-147">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="42856-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="42856-148">MOF</span><span class="sxs-lookup"><span data-stu-id="42856-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42856-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="42856-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42856-150">DLL</span><span class="sxs-lookup"><span data-stu-id="42856-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42856-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42856-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42856-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42856-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42856-153">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="42856-153">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

